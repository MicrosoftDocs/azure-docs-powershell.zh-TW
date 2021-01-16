---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
ms.openlocfilehash: a4b4ec4f24f61e188a3ab8b9cf66e8e326142bd3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274915"
---
# <span data-ttu-id="77846-101">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="77846-101">Stop-AzDataMigrationService</span></span>

## <span data-ttu-id="77846-102">摘要</span><span class="sxs-lookup"><span data-stu-id="77846-102">SYNOPSIS</span></span>
<span data-ttu-id="77846-103">停止處於執行中狀態的 Azure 資料庫移轉服務實例。</span><span class="sxs-lookup"><span data-stu-id="77846-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="77846-104">句法</span><span class="sxs-lookup"><span data-stu-id="77846-104">SYNTAX</span></span>

### <span data-ttu-id="77846-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="77846-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77846-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77846-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77846-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77846-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77846-108">說明</span><span class="sxs-lookup"><span data-stu-id="77846-108">DESCRIPTION</span></span>
<span data-ttu-id="77846-109">Stop-AzDataMigrationService Cmdlet 會停止處於執行中狀態的 Azure 資料庫移轉服務實例。</span><span class="sxs-lookup"><span data-stu-id="77846-109">The Stop-AzDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="77846-110">示例</span><span class="sxs-lookup"><span data-stu-id="77846-110">EXAMPLES</span></span>

### <span data-ttu-id="77846-111">範例1</span><span class="sxs-lookup"><span data-stu-id="77846-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="77846-112">上述範例會根據以輸入參數傳入的服務名稱來停止名為 TestService 的 Azure Database 遷移服務實例</span><span class="sxs-lookup"><span data-stu-id="77846-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="77846-113">範例2</span><span class="sxs-lookup"><span data-stu-id="77846-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="77846-114">上述範例會根據傳遞為輸入參數的 PSDataMigrationService 物件，來停止 Azure Database 遷移服務的實例。</span><span class="sxs-lookup"><span data-stu-id="77846-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>

## <span data-ttu-id="77846-115">參數</span><span class="sxs-lookup"><span data-stu-id="77846-115">PARAMETERS</span></span>

### <span data-ttu-id="77846-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77846-116">-DefaultProfile</span></span>
<span data-ttu-id="77846-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="77846-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77846-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77846-118">-InputObject</span></span>
<span data-ttu-id="77846-119">PSDataMigrationService 物件。</span><span class="sxs-lookup"><span data-stu-id="77846-119">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77846-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="77846-120">-Name</span></span>
<span data-ttu-id="77846-121">資料庫移轉服務名稱。</span><span class="sxs-lookup"><span data-stu-id="77846-121">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77846-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77846-122">-PassThru</span></span>
<span data-ttu-id="77846-123">會傳回 true/false。</span><span class="sxs-lookup"><span data-stu-id="77846-123">Returns an true/false.</span></span>
<span data-ttu-id="77846-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="77846-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="77846-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77846-125">-ResourceGroupName</span></span>
<span data-ttu-id="77846-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="77846-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77846-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77846-127">-ResourceId</span></span>
<span data-ttu-id="77846-128">DataMigrationService 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="77846-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="77846-129">-確認</span><span class="sxs-lookup"><span data-stu-id="77846-129">-Confirm</span></span>
<span data-ttu-id="77846-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="77846-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77846-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77846-131">-WhatIf</span></span>
<span data-ttu-id="77846-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="77846-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77846-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="77846-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77846-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77846-134">CommonParameters</span></span>
<span data-ttu-id="77846-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="77846-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77846-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="77846-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77846-137">輸入</span><span class="sxs-lookup"><span data-stu-id="77846-137">INPUTS</span></span>

### <span data-ttu-id="77846-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="77846-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="77846-139">System.object</span><span class="sxs-lookup"><span data-stu-id="77846-139">System.String</span></span>

## <span data-ttu-id="77846-140">輸出</span><span class="sxs-lookup"><span data-stu-id="77846-140">OUTPUTS</span></span>

### <span data-ttu-id="77846-141">System.object</span><span class="sxs-lookup"><span data-stu-id="77846-141">System.Boolean</span></span>

## <span data-ttu-id="77846-142">筆記</span><span class="sxs-lookup"><span data-stu-id="77846-142">NOTES</span></span>

## <span data-ttu-id="77846-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="77846-143">RELATED LINKS</span></span>