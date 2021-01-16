---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 8f83b199aae030bc0ff8cb8290bb6b273e0c8cff
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435349"
---
# <span data-ttu-id="59576-101">Get-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="59576-101">Get-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="59576-102">摘要</span><span class="sxs-lookup"><span data-stu-id="59576-102">SYNOPSIS</span></span>
<span data-ttu-id="59576-103">傳回指定 Kusto 群集和資料庫的資料庫主體清單。</span><span class="sxs-lookup"><span data-stu-id="59576-103">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="59576-104">句法</span><span class="sxs-lookup"><span data-stu-id="59576-104">SYNTAX</span></span>

```
Get-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="59576-105">說明</span><span class="sxs-lookup"><span data-stu-id="59576-105">DESCRIPTION</span></span>
<span data-ttu-id="59576-106">傳回指定 Kusto 群集和資料庫的資料庫主體清單。</span><span class="sxs-lookup"><span data-stu-id="59576-106">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="59576-107">示例</span><span class="sxs-lookup"><span data-stu-id="59576-107">EXAMPLES</span></span>

### <span data-ttu-id="59576-108">範例1：指定 Kusto 群集和資料庫的資料庫主體清單</span><span class="sxs-lookup"><span data-stu-id="59576-108">Example 1: List of database principals of the given Kusto cluster and database</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="59576-109">上述命令會傳回指定 Kusto 群集和資料庫的資料庫主體清單</span><span class="sxs-lookup"><span data-stu-id="59576-109">The above command returns a list of database principals of the given Kusto cluster and database</span></span>

## <span data-ttu-id="59576-110">參數</span><span class="sxs-lookup"><span data-stu-id="59576-110">PARAMETERS</span></span>

### <span data-ttu-id="59576-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="59576-111">-ClusterName</span></span>
<span data-ttu-id="59576-112">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="59576-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="59576-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="59576-113">-DatabaseName</span></span>
<span data-ttu-id="59576-114">Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="59576-114">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="59576-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59576-115">-DefaultProfile</span></span>
<span data-ttu-id="59576-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="59576-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59576-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59576-117">-ResourceGroupName</span></span>
<span data-ttu-id="59576-118">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="59576-118">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="59576-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="59576-119">-SubscriptionId</span></span>
<span data-ttu-id="59576-120">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="59576-120">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="59576-121">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="59576-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="59576-122">-確認</span><span class="sxs-lookup"><span data-stu-id="59576-122">-Confirm</span></span>
<span data-ttu-id="59576-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="59576-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59576-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59576-124">-WhatIf</span></span>
<span data-ttu-id="59576-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="59576-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59576-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="59576-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59576-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59576-127">CommonParameters</span></span>
<span data-ttu-id="59576-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="59576-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59576-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="59576-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59576-130">輸入</span><span class="sxs-lookup"><span data-stu-id="59576-130">INPUTS</span></span>

## <span data-ttu-id="59576-131">輸出</span><span class="sxs-lookup"><span data-stu-id="59576-131">OUTPUTS</span></span>

### <span data-ttu-id="59576-132">IDatabasePrincipal （Kusto）。 Api20200918。</span><span class="sxs-lookup"><span data-stu-id="59576-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span></span>

## <span data-ttu-id="59576-133">筆記</span><span class="sxs-lookup"><span data-stu-id="59576-133">NOTES</span></span>

<span data-ttu-id="59576-134">別名</span><span class="sxs-lookup"><span data-stu-id="59576-134">ALIASES</span></span>

## <span data-ttu-id="59576-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="59576-135">RELATED LINKS</span></span>
