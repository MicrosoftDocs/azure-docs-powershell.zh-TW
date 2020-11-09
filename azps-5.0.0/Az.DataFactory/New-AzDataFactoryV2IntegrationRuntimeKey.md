---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 07cb597f5ca3793e3eb8db3fe153fafaa94f3501
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285205"
---
# <span data-ttu-id="63fca-101">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="63fca-101">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="63fca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="63fca-102">SYNOPSIS</span></span>
<span data-ttu-id="63fca-103">重新產生自託管的整合執行時間金鑰。</span><span class="sxs-lookup"><span data-stu-id="63fca-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="63fca-104">句法</span><span class="sxs-lookup"><span data-stu-id="63fca-104">SYNTAX</span></span>

### <span data-ttu-id="63fca-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="63fca-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63fca-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="63fca-106">ByResourceId</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63fca-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="63fca-107">ByIntegrationRuntimeObject</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63fca-108">說明</span><span class="sxs-lookup"><span data-stu-id="63fca-108">DESCRIPTION</span></span>
<span data-ttu-id="63fca-109">Cmdlet **AzDataFactoryV2IntegrationRuntimeKey** 會再生整合執行時間金鑰，並使用由 "KeyName" 參數指定的金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="63fca-109">The cmdlet **New-AzDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="63fca-110">前一個金鑰將無效。</span><span class="sxs-lookup"><span data-stu-id="63fca-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="63fca-111">示例</span><span class="sxs-lookup"><span data-stu-id="63fca-111">EXAMPLES</span></span>

### <span data-ttu-id="63fca-112">範例1：為整合執行時間產生新的金鑰</span><span class="sxs-lookup"><span data-stu-id="63fca-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="63fca-113">這個 Cmdlet 會為集成執行時間（名為「test-selfhost-ir」）重新產生金鑰 ' authKey2」。</span><span class="sxs-lookup"><span data-stu-id="63fca-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="63fca-114">參數</span><span class="sxs-lookup"><span data-stu-id="63fca-114">PARAMETERS</span></span>

### <span data-ttu-id="63fca-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="63fca-115">-DataFactoryName</span></span>
<span data-ttu-id="63fca-116">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="63fca-116">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63fca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63fca-117">-DefaultProfile</span></span>
<span data-ttu-id="63fca-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="63fca-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63fca-119">-Force</span><span class="sxs-lookup"><span data-stu-id="63fca-119">-Force</span></span>
<span data-ttu-id="63fca-120">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="63fca-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="63fca-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63fca-121">-InputObject</span></span>
<span data-ttu-id="63fca-122">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="63fca-122">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63fca-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="63fca-123">-KeyName</span></span>
<span data-ttu-id="63fca-124">自託管整合執行時間的驗證金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="63fca-124">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63fca-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="63fca-125">-Name</span></span>
<span data-ttu-id="63fca-126">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="63fca-126">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63fca-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63fca-127">-ResourceGroupName</span></span>
<span data-ttu-id="63fca-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="63fca-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63fca-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63fca-129">-ResourceId</span></span>
<span data-ttu-id="63fca-130">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="63fca-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63fca-131">-確認</span><span class="sxs-lookup"><span data-stu-id="63fca-131">-Confirm</span></span>
<span data-ttu-id="63fca-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="63fca-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63fca-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63fca-133">-WhatIf</span></span>
<span data-ttu-id="63fca-134">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="63fca-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="63fca-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63fca-135">CommonParameters</span></span>
<span data-ttu-id="63fca-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="63fca-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63fca-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="63fca-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63fca-138">輸入</span><span class="sxs-lookup"><span data-stu-id="63fca-138">INPUTS</span></span>

### <span data-ttu-id="63fca-139">System.object</span><span class="sxs-lookup"><span data-stu-id="63fca-139">System.String</span></span>

### <span data-ttu-id="63fca-140">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="63fca-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="63fca-141">輸出</span><span class="sxs-lookup"><span data-stu-id="63fca-141">OUTPUTS</span></span>

### <span data-ttu-id="63fca-142">PSIntegrationRuntimeKeys 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="63fca-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="63fca-143">筆記</span><span class="sxs-lookup"><span data-stu-id="63fca-143">NOTES</span></span>

## <span data-ttu-id="63fca-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="63fca-144">RELATED LINKS</span></span>

[<span data-ttu-id="63fca-145">AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="63fca-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()