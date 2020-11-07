---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubKey.md
ms.openlocfilehash: 27be06fb85cc4bd1dc38dd7a123205d3ba7ff4d3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794777"
---
# <span data-ttu-id="31958-101">Get-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="31958-101">Get-AzEventHubKey</span></span>

## <span data-ttu-id="31958-102">摘要</span><span class="sxs-lookup"><span data-stu-id="31958-102">SYNOPSIS</span></span>
<span data-ttu-id="31958-103">取得指定事件中心授權規則的主要金鑰詳細資料。</span><span class="sxs-lookup"><span data-stu-id="31958-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="31958-104">句法</span><span class="sxs-lookup"><span data-stu-id="31958-104">SYNTAX</span></span>

### <span data-ttu-id="31958-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="31958-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31958-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="31958-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31958-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="31958-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31958-108">說明</span><span class="sxs-lookup"><span data-stu-id="31958-108">DESCRIPTION</span></span>
<span data-ttu-id="31958-109">Get-AzEventHubKey Cmdlet 會傳回主要和次要 connectionstrings 以及指定命名空間/事件中樞/別名授權規則的金鑰詳細資料。</span><span class="sxs-lookup"><span data-stu-id="31958-109">The Get-AzEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="31958-110">示例</span><span class="sxs-lookup"><span data-stu-id="31958-110">EXAMPLES</span></span>

### <span data-ttu-id="31958-111">範例 1-命名空間</span><span class="sxs-lookup"><span data-stu-id="31958-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="31958-112">範例 2-EventHub</span><span class="sxs-lookup"><span data-stu-id="31958-112">Example 2 - EventHub</span></span>
```
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="31958-113">取得授權規則 MyAuthRuleName 的主要和次要 connectionstrings 及金鑰的詳細 \` 資料 \` 。</span><span class="sxs-lookup"><span data-stu-id="31958-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="31958-114">範例 3-別名 (GeoRecovery 配置) </span><span class="sxs-lookup"><span data-stu-id="31958-114">Example 3 - Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="31958-115">取得授權規則 MyAuthRuleName 的主要、次要、AliasPrimary 和 AliasSecondary connectionstrings 及金鑰的詳細 \` 資料 \` 。</span><span class="sxs-lookup"><span data-stu-id="31958-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="31958-116">參數</span><span class="sxs-lookup"><span data-stu-id="31958-116">PARAMETERS</span></span>

### <span data-ttu-id="31958-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="31958-117">-AliasName</span></span>
<span data-ttu-id="31958-118">別名名稱</span><span class="sxs-lookup"><span data-stu-id="31958-118">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31958-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31958-119">-DefaultProfile</span></span>
<span data-ttu-id="31958-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="31958-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31958-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="31958-121">-EventHub</span></span>
<span data-ttu-id="31958-122">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="31958-122">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31958-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="31958-123">-Name</span></span>
<span data-ttu-id="31958-124">AuthorizationRule 名稱</span><span class="sxs-lookup"><span data-stu-id="31958-124">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31958-125">-命名空間</span><span class="sxs-lookup"><span data-stu-id="31958-125">-Namespace</span></span>
<span data-ttu-id="31958-126">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="31958-126">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31958-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31958-127">-ResourceGroupName</span></span>
<span data-ttu-id="31958-128">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="31958-128">Resource Group Name</span></span>

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

### <span data-ttu-id="31958-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31958-129">CommonParameters</span></span>
<span data-ttu-id="31958-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="31958-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31958-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="31958-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31958-132">輸入</span><span class="sxs-lookup"><span data-stu-id="31958-132">INPUTS</span></span>

### <span data-ttu-id="31958-133">System.object</span><span class="sxs-lookup"><span data-stu-id="31958-133">System.String</span></span>

## <span data-ttu-id="31958-134">輸出</span><span class="sxs-lookup"><span data-stu-id="31958-134">OUTPUTS</span></span>

### <span data-ttu-id="31958-135">PSListKeysAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="31958-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="31958-136">筆記</span><span class="sxs-lookup"><span data-stu-id="31958-136">NOTES</span></span>

## <span data-ttu-id="31958-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="31958-137">RELATED LINKS</span></span>