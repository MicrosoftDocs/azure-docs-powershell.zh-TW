---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
ms.openlocfilehash: 99dd311adf976e100282da92db6a3147880feefb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795905"
---
# <span data-ttu-id="8c191-101">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="8c191-101">Set-AzVMADDomainExtension</span></span>

## <span data-ttu-id="8c191-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c191-102">SYNOPSIS</span></span>
<span data-ttu-id="8c191-103">新增 AD 網域延伸至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8c191-103">Adds an AD domain extension to a virtual machine.</span></span>

## <span data-ttu-id="8c191-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c191-104">SYNTAX</span></span>

```
Set-AzVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c191-105">說明</span><span class="sxs-lookup"><span data-stu-id="8c191-105">DESCRIPTION</span></span>
<span data-ttu-id="8c191-106">**AzVMADDomainExtension** Cmdlet 會將 Azure Active DIRECTORY (AD) 網域虛擬電腦延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8c191-106">The **Set-AzVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="8c191-107">此延伸功能可讓您的虛擬機器加入網域。</span><span class="sxs-lookup"><span data-stu-id="8c191-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="8c191-108">示例</span><span class="sxs-lookup"><span data-stu-id="8c191-108">EXAMPLES</span></span>

## <span data-ttu-id="8c191-109">參數</span><span class="sxs-lookup"><span data-stu-id="8c191-109">PARAMETERS</span></span>

### <span data-ttu-id="8c191-110">-認證</span><span class="sxs-lookup"><span data-stu-id="8c191-110">-Credential</span></span>
<span data-ttu-id="8c191-111">指定虛擬機器的使用者名稱和密碼作為 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="8c191-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="8c191-112">若要取得認證，請使用 Get-Credential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c191-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="8c191-113">如需詳細資訊，請輸入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="8c191-113">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c191-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c191-114">-DefaultProfile</span></span>
<span data-ttu-id="8c191-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c191-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c191-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="8c191-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="8c191-117">表示此 Cmdlet 會停用延伸次要版本的自動升級。</span><span class="sxs-lookup"><span data-stu-id="8c191-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c191-118">-功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="8c191-118">-DomainName</span></span>
<span data-ttu-id="8c191-119">指定網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c191-119">Specifies the name of the domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c191-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="8c191-120">-ForceRerun</span></span>
<span data-ttu-id="8c191-121">表示此 Cmdlet 會強制在虛擬機器上重新執行相同的延伸設定，而不需卸載並重新安裝延伸。</span><span class="sxs-lookup"><span data-stu-id="8c191-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="8c191-122">這個值可以是與目前值不同的任何字串。</span><span class="sxs-lookup"><span data-stu-id="8c191-122">The value can be any string different from the current value.</span></span>

<span data-ttu-id="8c191-123">如果 forceUpdateTag 未變更，處理常式仍會套用公用或受保護設定的更新。</span><span class="sxs-lookup"><span data-stu-id="8c191-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c191-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="8c191-124">-JoinOption</span></span>
<span data-ttu-id="8c191-125">指定 [連接] 選項。</span><span class="sxs-lookup"><span data-stu-id="8c191-125">Specifies the join option.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c191-126">-位置</span><span class="sxs-lookup"><span data-stu-id="8c191-126">-Location</span></span>
<span data-ttu-id="8c191-127">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="8c191-127">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c191-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="8c191-128">-Name</span></span>
<span data-ttu-id="8c191-129">指定要新增之網域延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c191-129">Specifies the name of the domain extension to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c191-130">-OUPath</span><span class="sxs-lookup"><span data-stu-id="8c191-130">-OUPath</span></span>
<span data-ttu-id="8c191-131">指定網域帳戶 (OU) 的組織單位。</span><span class="sxs-lookup"><span data-stu-id="8c191-131">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="8c191-132">在引號中輸入 OU 的完整辨識名稱。</span><span class="sxs-lookup"><span data-stu-id="8c191-132">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="8c191-133">預設值是網域中電腦物件的預設 OU。</span><span class="sxs-lookup"><span data-stu-id="8c191-133">The default value is the default OU for machine objects in the domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c191-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c191-134">-ResourceGroupName</span></span>
<span data-ttu-id="8c191-135">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c191-135">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c191-136">-重新開機</span><span class="sxs-lookup"><span data-stu-id="8c191-136">-Restart</span></span>
<span data-ttu-id="8c191-137">表示此 Cmdlet 會重新開機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8c191-137">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="8c191-138">通常需要重新開機，才能使變更生效。</span><span class="sxs-lookup"><span data-stu-id="8c191-138">A restart is often required to make the change effective.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c191-139">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="8c191-139">-TypeHandlerVersion</span></span>
<span data-ttu-id="8c191-140">指定網域延伸的版本。</span><span class="sxs-lookup"><span data-stu-id="8c191-140">Specifies the version of the domain extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c191-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="8c191-141">-VMName</span></span>
<span data-ttu-id="8c191-142">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c191-142">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c191-143">-確認</span><span class="sxs-lookup"><span data-stu-id="8c191-143">-Confirm</span></span>
<span data-ttu-id="8c191-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8c191-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c191-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c191-145">-WhatIf</span></span>
<span data-ttu-id="8c191-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8c191-146">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="8c191-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c191-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c191-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c191-148">CommonParameters</span></span>
<span data-ttu-id="8c191-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c191-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c191-150">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8c191-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c191-151">輸入</span><span class="sxs-lookup"><span data-stu-id="8c191-151">INPUTS</span></span>

### <span data-ttu-id="8c191-152">所有</span><span class="sxs-lookup"><span data-stu-id="8c191-152">None</span></span>
<span data-ttu-id="8c191-153">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="8c191-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8c191-154">輸出</span><span class="sxs-lookup"><span data-stu-id="8c191-154">OUTPUTS</span></span>

### <span data-ttu-id="8c191-155">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="8c191-155">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="8c191-156">筆記</span><span class="sxs-lookup"><span data-stu-id="8c191-156">NOTES</span></span>

## <span data-ttu-id="8c191-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c191-157">RELATED LINKS</span></span>

[<span data-ttu-id="8c191-158">AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="8c191-158">Get-AzVMADDomainExtension</span></span>](./Get-AzVMADDomainExtension.md)