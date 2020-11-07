---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: d4741bc0456abfe99071f57d3224db8925bd1724
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791074"
---
# <span data-ttu-id="13ab8-101">Set-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="13ab8-101">Set-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="13ab8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="13ab8-102">SYNOPSIS</span></span>
<span data-ttu-id="13ab8-103">更新自動提供設定</span><span class="sxs-lookup"><span data-stu-id="13ab8-103">Updates automatic provisioning setting</span></span>

## <span data-ttu-id="13ab8-104">句法</span><span class="sxs-lookup"><span data-stu-id="13ab8-104">SYNTAX</span></span>

### <span data-ttu-id="13ab8-105">SubscriptionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="13ab8-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13ab8-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="13ab8-106">ResourceId</span></span>
```
Set-AzSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13ab8-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="13ab8-107">InputObject</span></span>
```
Set-AzSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13ab8-108">說明</span><span class="sxs-lookup"><span data-stu-id="13ab8-108">DESCRIPTION</span></span>
<span data-ttu-id="13ab8-109">開啟或關閉訂閱的自動預配設定。</span><span class="sxs-lookup"><span data-stu-id="13ab8-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="13ab8-110">自動提供設定可讓您決定是否要讓 Azure 安全中心自動建立將在 Vm 上安裝的安全代理程式。</span><span class="sxs-lookup"><span data-stu-id="13ab8-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="13ab8-111">安全性代理程式會監視您的 VM，以建立安全警示，並監視 VM 的安全性合規性。</span><span class="sxs-lookup"><span data-stu-id="13ab8-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="13ab8-112">示例</span><span class="sxs-lookup"><span data-stu-id="13ab8-112">EXAMPLES</span></span>

### <span data-ttu-id="13ab8-113">範例1</span><span class="sxs-lookup"><span data-stu-id="13ab8-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="13ab8-114">開啟訂閱的自動預配設定。</span><span class="sxs-lookup"><span data-stu-id="13ab8-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="13ab8-115">範例2</span><span class="sxs-lookup"><span data-stu-id="13ab8-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="13ab8-116">關閉訂閱的自動預配設定。</span><span class="sxs-lookup"><span data-stu-id="13ab8-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="13ab8-117">參數</span><span class="sxs-lookup"><span data-stu-id="13ab8-117">PARAMETERS</span></span>

### <span data-ttu-id="13ab8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13ab8-118">-DefaultProfile</span></span>
<span data-ttu-id="13ab8-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="13ab8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13ab8-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="13ab8-120">-EnableAutoProvision</span></span>
<span data-ttu-id="13ab8-121">自動提供。</span><span class="sxs-lookup"><span data-stu-id="13ab8-121">Automatic Provisioning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SubscriptionLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ab8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13ab8-122">-InputObject</span></span>
<span data-ttu-id="13ab8-123">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="13ab8-123">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13ab8-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="13ab8-124">-Name</span></span>
<span data-ttu-id="13ab8-125">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="13ab8-125">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ab8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13ab8-126">-ResourceId</span></span>
<span data-ttu-id="13ab8-127">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="13ab8-127">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13ab8-128">-確認</span><span class="sxs-lookup"><span data-stu-id="13ab8-128">-Confirm</span></span>
<span data-ttu-id="13ab8-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="13ab8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13ab8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13ab8-130">-WhatIf</span></span>
<span data-ttu-id="13ab8-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="13ab8-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13ab8-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="13ab8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13ab8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13ab8-133">CommonParameters</span></span>
<span data-ttu-id="13ab8-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="13ab8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13ab8-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="13ab8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13ab8-136">輸入</span><span class="sxs-lookup"><span data-stu-id="13ab8-136">INPUTS</span></span>

### <span data-ttu-id="13ab8-137">System.object</span><span class="sxs-lookup"><span data-stu-id="13ab8-137">System.String</span></span>

### <span data-ttu-id="13ab8-138">PSSecurityAutoProvisioningSetting 中的 AutoProvisioningSettings （Security..。</span><span class="sxs-lookup"><span data-stu-id="13ab8-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="13ab8-139">輸出</span><span class="sxs-lookup"><span data-stu-id="13ab8-139">OUTPUTS</span></span>

### <span data-ttu-id="13ab8-140">PSSecurityAutoProvisioningSetting 中的 AutoProvisioningSettings （Security..。</span><span class="sxs-lookup"><span data-stu-id="13ab8-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="13ab8-141">筆記</span><span class="sxs-lookup"><span data-stu-id="13ab8-141">NOTES</span></span>

## <span data-ttu-id="13ab8-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="13ab8-142">RELATED LINKS</span></span>