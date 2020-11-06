---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
ms.openlocfilehash: 2ec4ec1898e79fd7f7f35a406f2a99f9dd2da6fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622799"
---
# <span data-ttu-id="72f0c-101">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="72f0c-101">Get-AzVMADDomainExtension</span></span>

## <span data-ttu-id="72f0c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="72f0c-102">SYNOPSIS</span></span>
<span data-ttu-id="72f0c-103">取得有關 AD 網域延伸的資訊。</span><span class="sxs-lookup"><span data-stu-id="72f0c-103">Gets information about an AD domain extension.</span></span>

## <span data-ttu-id="72f0c-104">句法</span><span class="sxs-lookup"><span data-stu-id="72f0c-104">SYNTAX</span></span>

```
Get-AzVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72f0c-105">說明</span><span class="sxs-lookup"><span data-stu-id="72f0c-105">DESCRIPTION</span></span>
<span data-ttu-id="72f0c-106">**AzVMADDomainExtension** Cmdlet 會取得指定 Azure Active DIRECTORY (AD) 網域延伸的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="72f0c-106">The **Get-AzVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="72f0c-107">示例</span><span class="sxs-lookup"><span data-stu-id="72f0c-107">EXAMPLES</span></span>

## <span data-ttu-id="72f0c-108">參數</span><span class="sxs-lookup"><span data-stu-id="72f0c-108">PARAMETERS</span></span>

### <span data-ttu-id="72f0c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72f0c-109">-DefaultProfile</span></span>
<span data-ttu-id="72f0c-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="72f0c-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72f0c-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="72f0c-111">-Name</span></span>
<span data-ttu-id="72f0c-112">指定網域延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="72f0c-112">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="72f0c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72f0c-113">-ResourceGroupName</span></span>
<span data-ttu-id="72f0c-114">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="72f0c-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="72f0c-115">-狀態</span><span class="sxs-lookup"><span data-stu-id="72f0c-115">-Status</span></span>
<span data-ttu-id="72f0c-116">表示此 Cmdlet 會取得網域延伸的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="72f0c-116">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72f0c-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="72f0c-117">-VMName</span></span>
<span data-ttu-id="72f0c-118">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="72f0c-118">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="72f0c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72f0c-119">CommonParameters</span></span>
<span data-ttu-id="72f0c-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="72f0c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72f0c-121">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="72f0c-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72f0c-122">輸入</span><span class="sxs-lookup"><span data-stu-id="72f0c-122">INPUTS</span></span>

### <span data-ttu-id="72f0c-123">System.object</span><span class="sxs-lookup"><span data-stu-id="72f0c-123">System.String</span></span>

### <span data-ttu-id="72f0c-124">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="72f0c-124">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="72f0c-125">輸出</span><span class="sxs-lookup"><span data-stu-id="72f0c-125">OUTPUTS</span></span>

### <span data-ttu-id="72f0c-126">VirtualMachineADDomainExtensionCoNtext 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="72f0c-126">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="72f0c-127">筆記</span><span class="sxs-lookup"><span data-stu-id="72f0c-127">NOTES</span></span>

## <span data-ttu-id="72f0c-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="72f0c-128">RELATED LINKS</span></span>

[<span data-ttu-id="72f0c-129">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="72f0c-129">Set-AzVMADDomainExtension</span></span>](./Set-AzVMADDomainExtension.md)

