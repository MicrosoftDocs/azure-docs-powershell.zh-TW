---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 9137b62098a1441cea8acc53c52c0e0ea835ff09
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796270"
---
# <span data-ttu-id="28cde-101">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="28cde-101">Get-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="28cde-102">摘要</span><span class="sxs-lookup"><span data-stu-id="28cde-102">SYNOPSIS</span></span>
<span data-ttu-id="28cde-103">取得虛擬機器上的診斷延伸設定。</span><span class="sxs-lookup"><span data-stu-id="28cde-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="28cde-104">句法</span><span class="sxs-lookup"><span data-stu-id="28cde-104">SYNTAX</span></span>

```
Get-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28cde-105">說明</span><span class="sxs-lookup"><span data-stu-id="28cde-105">DESCRIPTION</span></span>
<span data-ttu-id="28cde-106">**AzVMDiagnosticsExtension** Cmdlet 會取得虛擬機器上 Azure Diagnostics 延伸的設定。</span><span class="sxs-lookup"><span data-stu-id="28cde-106">The **Get-AzVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="28cde-107">示例</span><span class="sxs-lookup"><span data-stu-id="28cde-107">EXAMPLES</span></span>

### <span data-ttu-id="28cde-108">範例1：取得套用至虛擬機器的診斷延伸</span><span class="sxs-lookup"><span data-stu-id="28cde-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="28cde-109">這個命令會取得已套用到名為 ContosoVM22 的虛擬機器的診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="28cde-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="28cde-110">參數</span><span class="sxs-lookup"><span data-stu-id="28cde-110">PARAMETERS</span></span>

### <span data-ttu-id="28cde-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28cde-111">-DefaultProfile</span></span>
<span data-ttu-id="28cde-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="28cde-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28cde-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="28cde-113">-Name</span></span>
<span data-ttu-id="28cde-114">指定此 Cmdlet 取得其設定的診斷延伸名稱。</span><span class="sxs-lookup"><span data-stu-id="28cde-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28cde-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28cde-115">-ResourceGroupName</span></span>
<span data-ttu-id="28cde-116">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="28cde-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="28cde-117">-狀態</span><span class="sxs-lookup"><span data-stu-id="28cde-117">-Status</span></span>
<span data-ttu-id="28cde-118">指示此 Cmdlet 使用 Status 值。</span><span class="sxs-lookup"><span data-stu-id="28cde-118">Indicates that this cmdlet uses the Status value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28cde-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="28cde-119">-VMName</span></span>
<span data-ttu-id="28cde-120">指定此 Cmdlet 取得診斷延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="28cde-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="28cde-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28cde-121">CommonParameters</span></span>
<span data-ttu-id="28cde-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="28cde-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28cde-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="28cde-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28cde-124">輸入</span><span class="sxs-lookup"><span data-stu-id="28cde-124">INPUTS</span></span>

### <span data-ttu-id="28cde-125">所有</span><span class="sxs-lookup"><span data-stu-id="28cde-125">None</span></span>
<span data-ttu-id="28cde-126">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="28cde-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="28cde-127">輸出</span><span class="sxs-lookup"><span data-stu-id="28cde-127">OUTPUTS</span></span>

### <span data-ttu-id="28cde-128">PSVirtualMachineExtension 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="28cde-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="28cde-129">筆記</span><span class="sxs-lookup"><span data-stu-id="28cde-129">NOTES</span></span>

## <span data-ttu-id="28cde-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="28cde-130">RELATED LINKS</span></span>

[<span data-ttu-id="28cde-131">移除-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="28cde-131">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="28cde-132">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="28cde-132">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

