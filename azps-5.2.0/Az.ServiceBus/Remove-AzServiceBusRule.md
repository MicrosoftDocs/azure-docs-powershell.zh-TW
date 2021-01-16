---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
ms.openlocfilehash: a3fc0d37e48ddeba41b6870edfe1732eeecfaa14
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276096"
---
# <span data-ttu-id="1a60f-101">Remove-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="1a60f-101">Remove-AzServiceBusRule</span></span>

## <span data-ttu-id="1a60f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1a60f-102">SYNOPSIS</span></span>
<span data-ttu-id="1a60f-103">移除指定訂閱的指定規則。</span><span class="sxs-lookup"><span data-stu-id="1a60f-103">Removes the specified rule of a given subscription .</span></span>

## <span data-ttu-id="1a60f-104">句法</span><span class="sxs-lookup"><span data-stu-id="1a60f-104">SYNTAX</span></span>

### <span data-ttu-id="1a60f-105">RulePropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1a60f-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a60f-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1a60f-106">RuleResourceIdSet</span></span>
```
Remove-AzServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a60f-107">說明</span><span class="sxs-lookup"><span data-stu-id="1a60f-107">DESCRIPTION</span></span>
<span data-ttu-id="1a60f-108">**AzServiceBusRule** Cmdlet 會移除指定主題的訂閱規則。</span><span class="sxs-lookup"><span data-stu-id="1a60f-108">The **Remove-AzServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="1a60f-109">示例</span><span class="sxs-lookup"><span data-stu-id="1a60f-109">EXAMPLES</span></span>

### <span data-ttu-id="1a60f-110">範例1</span><span class="sxs-lookup"><span data-stu-id="1a60f-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="1a60f-111">移除 `SBRule` 指定主題的訂閱規則 `SBSubscription` `SBTopic` 。</span><span class="sxs-lookup"><span data-stu-id="1a60f-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="1a60f-112">範例2：使用 InputObject 的變數：</span><span class="sxs-lookup"><span data-stu-id="1a60f-112">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="1a60f-113">移除透過 $inputobject for-InputObject 參數提供的規則</span><span class="sxs-lookup"><span data-stu-id="1a60f-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="1a60f-114">範例3：使用 [InputObject] 管道：</span><span class="sxs-lookup"><span data-stu-id="1a60f-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusRule <params> | Remove-AzServiceBusRule
```

### <span data-ttu-id="1a60f-115">範例4：使用變數 ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a60f-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="1a60f-116">範例5：使用中的字串值</span><span class="sxs-lookup"><span data-stu-id="1a60f-116">Example 5: ResourceId - Using string value</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="1a60f-117">在 $resourceid/string 中移除透過 ARM Id 提供的規則</span><span class="sxs-lookup"><span data-stu-id="1a60f-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="1a60f-118">參數</span><span class="sxs-lookup"><span data-stu-id="1a60f-118">PARAMETERS</span></span>

### <span data-ttu-id="1a60f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a60f-119">-AsJob</span></span>
<span data-ttu-id="1a60f-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1a60f-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a60f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a60f-121">-DefaultProfile</span></span>
<span data-ttu-id="1a60f-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1a60f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a60f-123">-Force</span><span class="sxs-lookup"><span data-stu-id="1a60f-123">-Force</span></span>
<span data-ttu-id="1a60f-124">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="1a60f-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1a60f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a60f-125">-InputObject</span></span>
<span data-ttu-id="1a60f-126">服務匯流排規則物件</span><span class="sxs-lookup"><span data-stu-id="1a60f-126">Service Bus Rule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: RuleResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a60f-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="1a60f-127">-Name</span></span>
<span data-ttu-id="1a60f-128">規則名稱</span><span class="sxs-lookup"><span data-stu-id="1a60f-128">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a60f-129">-命名空間</span><span class="sxs-lookup"><span data-stu-id="1a60f-129">-Namespace</span></span>
<span data-ttu-id="1a60f-130">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="1a60f-130">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a60f-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a60f-131">-PassThru</span></span>
<span data-ttu-id="1a60f-132">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="1a60f-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="1a60f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a60f-133">-ResourceGroupName</span></span>
<span data-ttu-id="1a60f-134">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="1a60f-134">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a60f-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a60f-135">-ResourceId</span></span>
<span data-ttu-id="1a60f-136">服務匯流排規則資源識別碼</span><span class="sxs-lookup"><span data-stu-id="1a60f-136">Service Bus Rule Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: RuleResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a60f-137">-訂閱</span><span class="sxs-lookup"><span data-stu-id="1a60f-137">-Subscription</span></span>
<span data-ttu-id="1a60f-138">訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="1a60f-138">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a60f-139">-主題</span><span class="sxs-lookup"><span data-stu-id="1a60f-139">-Topic</span></span>
<span data-ttu-id="1a60f-140">主題名稱</span><span class="sxs-lookup"><span data-stu-id="1a60f-140">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a60f-141">-確認</span><span class="sxs-lookup"><span data-stu-id="1a60f-141">-Confirm</span></span>
<span data-ttu-id="1a60f-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1a60f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a60f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a60f-143">-WhatIf</span></span>
<span data-ttu-id="1a60f-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1a60f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a60f-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1a60f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a60f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a60f-146">CommonParameters</span></span>
<span data-ttu-id="1a60f-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1a60f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a60f-148">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1a60f-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a60f-149">輸入</span><span class="sxs-lookup"><span data-stu-id="1a60f-149">INPUTS</span></span>

### <span data-ttu-id="1a60f-150">System.object</span><span class="sxs-lookup"><span data-stu-id="1a60f-150">System.String</span></span>

### <span data-ttu-id="1a60f-151">PSTopicAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1a60f-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="1a60f-152">輸出</span><span class="sxs-lookup"><span data-stu-id="1a60f-152">OUTPUTS</span></span>

### <span data-ttu-id="1a60f-153">System.object</span><span class="sxs-lookup"><span data-stu-id="1a60f-153">System.Boolean</span></span>

## <span data-ttu-id="1a60f-154">筆記</span><span class="sxs-lookup"><span data-stu-id="1a60f-154">NOTES</span></span>

## <span data-ttu-id="1a60f-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="1a60f-155">RELATED LINKS</span></span>