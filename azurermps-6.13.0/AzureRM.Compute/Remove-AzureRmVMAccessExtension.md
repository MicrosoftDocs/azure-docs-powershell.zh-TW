---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
ms.openlocfilehash: 0360bcdb766de681ab6f54682007076e18266051
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623565"
---
# <span data-ttu-id="371eb-101">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="371eb-101">Remove-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="371eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="371eb-102">SYNOPSIS</span></span>
<span data-ttu-id="371eb-103">從虛擬機器移除 VMAccess 延伸。</span><span class="sxs-lookup"><span data-stu-id="371eb-103">Removes the VMAccess extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="371eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="371eb-104">SYNTAX</span></span>

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="371eb-105">說明</span><span class="sxs-lookup"><span data-stu-id="371eb-105">DESCRIPTION</span></span>
<span data-ttu-id="371eb-106">**AzureRmVMAccessExtension** Cmdlet 會從虛擬機器中移除虛擬機器存取 (VMAccess) 虛擬電腦延伸。</span><span class="sxs-lookup"><span data-stu-id="371eb-106">The **Remove-AzureRmVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="371eb-107">示例</span><span class="sxs-lookup"><span data-stu-id="371eb-107">EXAMPLES</span></span>

## <span data-ttu-id="371eb-108">參數</span><span class="sxs-lookup"><span data-stu-id="371eb-108">PARAMETERS</span></span>

### <span data-ttu-id="371eb-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="371eb-109">-DefaultProfile</span></span>
<span data-ttu-id="371eb-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="371eb-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="371eb-111">-Force</span><span class="sxs-lookup"><span data-stu-id="371eb-111">-Force</span></span>
<span data-ttu-id="371eb-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="371eb-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="371eb-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="371eb-113">-Name</span></span>
<span data-ttu-id="371eb-114">指定此 Cmdlet 移除的延伸名稱。</span><span class="sxs-lookup"><span data-stu-id="371eb-114">Specifies the name of the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="371eb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="371eb-115">-ResourceGroupName</span></span>
<span data-ttu-id="371eb-116">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="371eb-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="371eb-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="371eb-117">-VMName</span></span>
<span data-ttu-id="371eb-118">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="371eb-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="371eb-119">這個 Cmdlet 會移除此參數指定之虛擬機器的 VMAccess。</span><span class="sxs-lookup"><span data-stu-id="371eb-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="371eb-120">-確認</span><span class="sxs-lookup"><span data-stu-id="371eb-120">-Confirm</span></span>
<span data-ttu-id="371eb-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="371eb-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="371eb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="371eb-122">-WhatIf</span></span>
<span data-ttu-id="371eb-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="371eb-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="371eb-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="371eb-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="371eb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="371eb-125">CommonParameters</span></span>
<span data-ttu-id="371eb-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="371eb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="371eb-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="371eb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="371eb-128">輸入</span><span class="sxs-lookup"><span data-stu-id="371eb-128">INPUTS</span></span>

### <span data-ttu-id="371eb-129">System.object</span><span class="sxs-lookup"><span data-stu-id="371eb-129">System.String</span></span>

## <span data-ttu-id="371eb-130">輸出</span><span class="sxs-lookup"><span data-stu-id="371eb-130">OUTPUTS</span></span>

### <span data-ttu-id="371eb-131">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="371eb-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="371eb-132">筆記</span><span class="sxs-lookup"><span data-stu-id="371eb-132">NOTES</span></span>

## <span data-ttu-id="371eb-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="371eb-133">RELATED LINKS</span></span>

[<span data-ttu-id="371eb-134">AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="371eb-134">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="371eb-135">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="371eb-135">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="371eb-136">移除-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="371eb-136">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)