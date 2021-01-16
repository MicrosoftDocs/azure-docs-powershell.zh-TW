---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
ms.openlocfilehash: a89d762f0317075a0da94290ad964aeef133fdd5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435324"
---
# <span data-ttu-id="f38af-101">Get-AzMigrateReplicationProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f38af-101">Get-AzMigrateReplicationProtectionContainer</span></span>

## <span data-ttu-id="f38af-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f38af-102">SYNOPSIS</span></span>
<span data-ttu-id="f38af-103">取得保護容器的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f38af-103">Gets the details of a protection container.</span></span>

## <span data-ttu-id="f38af-104">句法</span><span class="sxs-lookup"><span data-stu-id="f38af-104">SYNTAX</span></span>

### <span data-ttu-id="f38af-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="f38af-105">List (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainer -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f38af-106">獲取</span><span class="sxs-lookup"><span data-stu-id="f38af-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f38af-107">List1</span><span class="sxs-lookup"><span data-stu-id="f38af-107">List1</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ResourceGroupName <String>
 -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f38af-108">說明</span><span class="sxs-lookup"><span data-stu-id="f38af-108">DESCRIPTION</span></span>
<span data-ttu-id="f38af-109">取得保護容器的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f38af-109">Gets the details of a protection container.</span></span>

## <span data-ttu-id="f38af-110">示例</span><span class="sxs-lookup"><span data-stu-id="f38af-110">EXAMPLES</span></span>

### <span data-ttu-id="f38af-111">範例1：列出保存庫和結構中的所有保護容器</span><span class="sxs-lookup"><span data-stu-id="f38af-111">Example 1: List all protection containers in vault and fabric</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="f38af-112">列出全部。</span><span class="sxs-lookup"><span data-stu-id="f38af-112">Lists all.</span></span>

### <span data-ttu-id="f38af-113">範例2：取得特定的容器</span><span class="sxs-lookup"><span data-stu-id="f38af-113">Example 2: Get a specific container</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="f38af-114">取得特定的專案。</span><span class="sxs-lookup"><span data-stu-id="f38af-114">Gets a specific one.</span></span>

## <span data-ttu-id="f38af-115">參數</span><span class="sxs-lookup"><span data-stu-id="f38af-115">PARAMETERS</span></span>

### <span data-ttu-id="f38af-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f38af-116">-DefaultProfile</span></span>
<span data-ttu-id="f38af-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f38af-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f38af-118">-FabricName</span><span class="sxs-lookup"><span data-stu-id="f38af-118">-FabricName</span></span>
<span data-ttu-id="f38af-119">Fabric name。</span><span class="sxs-lookup"><span data-stu-id="f38af-119">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f38af-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="f38af-120">-ProtectionContainerName</span></span>
<span data-ttu-id="f38af-121">保護容器名稱。</span><span class="sxs-lookup"><span data-stu-id="f38af-121">Protection container name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f38af-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f38af-122">-ResourceGroupName</span></span>
<span data-ttu-id="f38af-123">[恢復服務] 電子倉庫所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f38af-123">The name of the resource group where the recovery services vault is present.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f38af-124">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="f38af-124">-ResourceName</span></span>
<span data-ttu-id="f38af-125">[恢復服務] 保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f38af-125">The name of the recovery services vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f38af-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f38af-126">-SubscriptionId</span></span>
<span data-ttu-id="f38af-127">訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="f38af-127">The subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f38af-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f38af-128">CommonParameters</span></span>
<span data-ttu-id="f38af-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f38af-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f38af-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f38af-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f38af-131">輸入</span><span class="sxs-lookup"><span data-stu-id="f38af-131">INPUTS</span></span>

## <span data-ttu-id="f38af-132">輸出</span><span class="sxs-lookup"><span data-stu-id="f38af-132">OUTPUTS</span></span>

### <span data-ttu-id="f38af-133">IProtectionContainer 中的 Api20180110 （）。</span><span class="sxs-lookup"><span data-stu-id="f38af-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span></span>

## <span data-ttu-id="f38af-134">筆記</span><span class="sxs-lookup"><span data-stu-id="f38af-134">NOTES</span></span>

<span data-ttu-id="f38af-135">別名</span><span class="sxs-lookup"><span data-stu-id="f38af-135">ALIASES</span></span>

## <span data-ttu-id="f38af-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="f38af-136">RELATED LINKS</span></span>
