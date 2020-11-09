---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayHybridConnection.md
ms.openlocfilehash: 2b029b2a93a063a322c11ea84cd46b787acc9960
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287300"
---
# <span data-ttu-id="6320d-101">Set-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="6320d-101">Set-AzRelayHybridConnection</span></span>

## <span data-ttu-id="6320d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6320d-102">SYNOPSIS</span></span>
<span data-ttu-id="6320d-103">更新指定的中繼命名空間中 HybridConnection 的描述。</span><span class="sxs-lookup"><span data-stu-id="6320d-103">Updates the description of a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="6320d-104">句法</span><span class="sxs-lookup"><span data-stu-id="6320d-104">SYNTAX</span></span>

### <span data-ttu-id="6320d-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6320d-105">HybridConnectionInputObjectSet</span></span>
```
Set-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6320d-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="6320d-106">HybridConnectionPropertiesSet</span></span>
```
Set-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6320d-107">說明</span><span class="sxs-lookup"><span data-stu-id="6320d-107">DESCRIPTION</span></span>
<span data-ttu-id="6320d-108">Set-AzRelayHybridConnection Cmdlet 會更新指定的中繼命名空間中 HybridConnection 的描述。</span><span class="sxs-lookup"><span data-stu-id="6320d-108">The Set-AzRelayHybridConnection cmdlet updates the description for the HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="6320d-109">示例</span><span class="sxs-lookup"><span data-stu-id="6320d-109">EXAMPLES</span></span>

### <span data-ttu-id="6320d-110">範例1</span><span class="sxs-lookup"><span data-stu-id="6320d-110">Example 1</span></span>
```
PS C:\>
PS C:\> $GetHybrid = Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
PS C:\> $GetHybrid.UserMetadata = "Test UserMetadata"
PS C:\> Set-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -InputObject $GetHybrid

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:08:11 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : Test UserMetadata
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n2
Name                        : TestHybirdConnection2
Type                        : Microsoft.Relay/HybridConnections
```

### <span data-ttu-id="6320d-111">範例2</span><span class="sxs-lookup"><span data-stu-id="6320d-111">Example 2</span></span>
```
PS C:\> Set-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -UserMetadata = "Test UserMetadata updated"

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:10:25 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : Test UserMetadata updated
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n1
Name                        : TestHybirdConnection1
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="6320d-112">使用指定命名空間中的新描述更新指定的 HybridConnection。</span><span class="sxs-lookup"><span data-stu-id="6320d-112">Updates the specified HybridConnection with a new description in the specified namespace.</span></span>
<span data-ttu-id="6320d-113">這個範例會使用新的值更新 UserMetadata 屬性。</span><span class="sxs-lookup"><span data-stu-id="6320d-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="6320d-114">參數</span><span class="sxs-lookup"><span data-stu-id="6320d-114">PARAMETERS</span></span>

### <span data-ttu-id="6320d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6320d-115">-DefaultProfile</span></span>
<span data-ttu-id="6320d-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6320d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6320d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6320d-117">-InputObject</span></span>
<span data-ttu-id="6320d-118">HybridConnections 物件。</span><span class="sxs-lookup"><span data-stu-id="6320d-118">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes
Parameter Sets: HybridConnectionInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6320d-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="6320d-119">-Name</span></span>
<span data-ttu-id="6320d-120">HybridConnections [名稱]。</span><span class="sxs-lookup"><span data-stu-id="6320d-120">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6320d-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="6320d-121">-Namespace</span></span>
<span data-ttu-id="6320d-122">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="6320d-122">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6320d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6320d-123">-ResourceGroupName</span></span>
<span data-ttu-id="6320d-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="6320d-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="6320d-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="6320d-125">-UserMetadata</span></span>
<span data-ttu-id="6320d-126">取得或設定 usermetadata 是一個預留位置，用來儲存 HybridConnection 端點的使用者定義字串資料。例如，它可以用來儲存描述性資料，例如小組清單和連絡人資訊，也可以儲存使用者定義的設定設定。</span><span class="sxs-lookup"><span data-stu-id="6320d-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6320d-127">-確認</span><span class="sxs-lookup"><span data-stu-id="6320d-127">-Confirm</span></span>
<span data-ttu-id="6320d-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6320d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6320d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6320d-129">-WhatIf</span></span>
<span data-ttu-id="6320d-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6320d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6320d-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6320d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6320d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6320d-132">CommonParameters</span></span>
<span data-ttu-id="6320d-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6320d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6320d-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6320d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6320d-135">輸入</span><span class="sxs-lookup"><span data-stu-id="6320d-135">INPUTS</span></span>

### <span data-ttu-id="6320d-136">System.object</span><span class="sxs-lookup"><span data-stu-id="6320d-136">System.String</span></span>

### <span data-ttu-id="6320d-137">PSHybridConnectionAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6320d-137">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="6320d-138">輸出</span><span class="sxs-lookup"><span data-stu-id="6320d-138">OUTPUTS</span></span>

### <span data-ttu-id="6320d-139">PSHybridConnectionAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6320d-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="6320d-140">筆記</span><span class="sxs-lookup"><span data-stu-id="6320d-140">NOTES</span></span>

## <span data-ttu-id="6320d-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="6320d-141">RELATED LINKS</span></span>