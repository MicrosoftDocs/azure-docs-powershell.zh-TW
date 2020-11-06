---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: fd87311c59c0889a57cb22eb08aba855e5c3b49c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620656"
---
# <span data-ttu-id="8bb60-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="8bb60-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="8bb60-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8bb60-102">SYNOPSIS</span></span>
<span data-ttu-id="8bb60-103">檢索主要或次要命名空間的別名 (災害復原設定) </span><span class="sxs-lookup"><span data-stu-id="8bb60-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="8bb60-104">句法</span><span class="sxs-lookup"><span data-stu-id="8bb60-104">SYNTAX</span></span>

### <span data-ttu-id="8bb60-105">GeoDRPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8bb60-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8bb60-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8bb60-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8bb60-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bb60-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bb60-108">說明</span><span class="sxs-lookup"><span data-stu-id="8bb60-108">DESCRIPTION</span></span>
<span data-ttu-id="8bb60-109">**AzServiceBusGeoDRConfiguration** 會在主要或次要命名空間中檢索別名 (災害復原配置) </span><span class="sxs-lookup"><span data-stu-id="8bb60-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="8bb60-110">示例</span><span class="sxs-lookup"><span data-stu-id="8bb60-110">EXAMPLES</span></span>

### <span data-ttu-id="8bb60-111">範例1</span><span class="sxs-lookup"><span data-stu-id="8bb60-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="8bb60-112">針對主要命名空間 "SampleNamespace_Primary" 檢索別名 "SampleDRCongifName" 設定</span><span class="sxs-lookup"><span data-stu-id="8bb60-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="8bb60-113">參數</span><span class="sxs-lookup"><span data-stu-id="8bb60-113">PARAMETERS</span></span>

### <span data-ttu-id="8bb60-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bb60-114">-DefaultProfile</span></span>
<span data-ttu-id="8bb60-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8bb60-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bb60-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bb60-116">-InputObject</span></span>
<span data-ttu-id="8bb60-117">Namespace 物件</span><span class="sxs-lookup"><span data-stu-id="8bb60-117">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb60-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="8bb60-118">-Name</span></span>
<span data-ttu-id="8bb60-119">DR 配置名稱</span><span class="sxs-lookup"><span data-stu-id="8bb60-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="8bb60-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="8bb60-120">-Namespace</span></span>
<span data-ttu-id="8bb60-121">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="8bb60-121">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb60-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bb60-122">-ResourceGroupName</span></span>
<span data-ttu-id="8bb60-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="8bb60-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb60-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bb60-124">-ResourceId</span></span>
<span data-ttu-id="8bb60-125">命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="8bb60-125">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb60-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bb60-126">CommonParameters</span></span>
<span data-ttu-id="8bb60-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8bb60-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bb60-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8bb60-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bb60-129">輸入</span><span class="sxs-lookup"><span data-stu-id="8bb60-129">INPUTS</span></span>

### <span data-ttu-id="8bb60-130">System.object</span><span class="sxs-lookup"><span data-stu-id="8bb60-130">System.String</span></span>

### <span data-ttu-id="8bb60-131">PSNamespaceAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8bb60-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="8bb60-132">輸出</span><span class="sxs-lookup"><span data-stu-id="8bb60-132">OUTPUTS</span></span>

### <span data-ttu-id="8bb60-133">PSServiceBusDRConfigurationAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8bb60-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="8bb60-134">筆記</span><span class="sxs-lookup"><span data-stu-id="8bb60-134">NOTES</span></span>

## <span data-ttu-id="8bb60-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="8bb60-135">RELATED LINKS</span></span>