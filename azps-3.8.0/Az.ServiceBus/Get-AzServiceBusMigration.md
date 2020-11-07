---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
ms.openlocfilehash: 686a2486d6a5e28e0149eb8fbf2387744d545fd0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959693"
---
# <span data-ttu-id="5984a-101">Get-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="5984a-101">Get-AzServiceBusMigration</span></span>

## <span data-ttu-id="5984a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5984a-102">SYNOPSIS</span></span>
<span data-ttu-id="5984a-103">檢索命名空間的 MigrationConfiguration</span><span class="sxs-lookup"><span data-stu-id="5984a-103">Retrieves MigrationConfiguration for the namespace</span></span>

## <span data-ttu-id="5984a-104">句法</span><span class="sxs-lookup"><span data-stu-id="5984a-104">SYNTAX</span></span>

### <span data-ttu-id="5984a-105">MigrationConfigurationPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5984a-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5984a-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5984a-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusMigration [-InputObject] <PSNamespaceAttributes> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5984a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5984a-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5984a-108">說明</span><span class="sxs-lookup"><span data-stu-id="5984a-108">DESCRIPTION</span></span>
<span data-ttu-id="5984a-109">**AzServiceBusMigration** 會檢索命名空間的遷移設定</span><span class="sxs-lookup"><span data-stu-id="5984a-109">The **Get-AzServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="5984a-110">示例</span><span class="sxs-lookup"><span data-stu-id="5984a-110">EXAMPLES</span></span>

### <span data-ttu-id="5984a-111">範例1</span><span class="sxs-lookup"><span data-stu-id="5984a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Succeeded
PendingReplicationOperationsCount : 40
TargetNamespace   : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="5984a-112">取得 ' TestingNamespaceStandardMigration」的遷移設定屬性</span><span class="sxs-lookup"><span data-stu-id="5984a-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMigration'</span></span>

## <span data-ttu-id="5984a-113">參數</span><span class="sxs-lookup"><span data-stu-id="5984a-113">PARAMETERS</span></span>

### <span data-ttu-id="5984a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5984a-114">-DefaultProfile</span></span>
<span data-ttu-id="5984a-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5984a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5984a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5984a-116">-InputObject</span></span>
<span data-ttu-id="5984a-117">Namespace 物件</span><span class="sxs-lookup"><span data-stu-id="5984a-117">Namespace Object</span></span>

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

### <span data-ttu-id="5984a-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="5984a-118">-Name</span></span>
<span data-ttu-id="5984a-119">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="5984a-119">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5984a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5984a-120">-ResourceGroupName</span></span>
<span data-ttu-id="5984a-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="5984a-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5984a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5984a-122">-ResourceId</span></span>
<span data-ttu-id="5984a-123">命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="5984a-123">Namespace Resource Id</span></span>

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

### <span data-ttu-id="5984a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5984a-124">CommonParameters</span></span>
<span data-ttu-id="5984a-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5984a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5984a-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5984a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5984a-127">輸入</span><span class="sxs-lookup"><span data-stu-id="5984a-127">INPUTS</span></span>

### <span data-ttu-id="5984a-128">PSNamespaceAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5984a-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="5984a-129">System.object</span><span class="sxs-lookup"><span data-stu-id="5984a-129">System.String</span></span>

## <span data-ttu-id="5984a-130">輸出</span><span class="sxs-lookup"><span data-stu-id="5984a-130">OUTPUTS</span></span>

### <span data-ttu-id="5984a-131">PSServiceBusMigrationConfigurationAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5984a-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="5984a-132">筆記</span><span class="sxs-lookup"><span data-stu-id="5984a-132">NOTES</span></span>

## <span data-ttu-id="5984a-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="5984a-133">RELATED LINKS</span></span>