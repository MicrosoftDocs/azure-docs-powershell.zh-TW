---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmbootdiagnosticsdata
schema: 2.0.0
ms.openlocfilehash: 867f2c14e90eddd9649e0720d41f56aa896c61ff
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800546"
---
# <span data-ttu-id="23d7c-101">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="23d7c-101">Get-AzureRmVMBootDiagnosticsData</span></span>

## <span data-ttu-id="23d7c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23d7c-102">SYNOPSIS</span></span>
<span data-ttu-id="23d7c-103">取得虛擬機器的啟動診斷資料。</span><span class="sxs-lookup"><span data-stu-id="23d7c-103">Gets boot diagnostics data for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23d7c-104">句法</span><span class="sxs-lookup"><span data-stu-id="23d7c-104">SYNTAX</span></span>

### <span data-ttu-id="23d7c-105">WindowsParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="23d7c-105">WindowsParamSet (Default)</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23d7c-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="23d7c-106">LinuxParamSet</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23d7c-107">說明</span><span class="sxs-lookup"><span data-stu-id="23d7c-107">DESCRIPTION</span></span>
<span data-ttu-id="23d7c-108">**AzureRmVMBootDiagnosticsData** Cmdlet 會取得虛擬機器的啟動診斷資料。</span><span class="sxs-lookup"><span data-stu-id="23d7c-108">The **Get-AzureRmVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="23d7c-109">示例</span><span class="sxs-lookup"><span data-stu-id="23d7c-109">EXAMPLES</span></span>

### <span data-ttu-id="23d7c-110">範例1：取得啟動診斷資料</span><span class="sxs-lookup"><span data-stu-id="23d7c-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzureRmVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="23d7c-111">這個命令會取得名為 ContosoVM07 的虛擬機器的啟動診斷資料。</span><span class="sxs-lookup"><span data-stu-id="23d7c-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="23d7c-112">此虛擬機器會執行 Windows 作業系統。</span><span class="sxs-lookup"><span data-stu-id="23d7c-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="23d7c-113">該命令會將資料儲存在指定的本機路徑中。</span><span class="sxs-lookup"><span data-stu-id="23d7c-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="23d7c-114">參數</span><span class="sxs-lookup"><span data-stu-id="23d7c-114">PARAMETERS</span></span>

### <span data-ttu-id="23d7c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23d7c-115">-DefaultProfile</span></span>
<span data-ttu-id="23d7c-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="23d7c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23d7c-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="23d7c-117">-Linux</span></span>
<span data-ttu-id="23d7c-118">表示虛擬機器執行的是 Linux 作業系統。</span><span class="sxs-lookup"><span data-stu-id="23d7c-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LinuxParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d7c-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="23d7c-119">-LocalPath</span></span>
<span data-ttu-id="23d7c-120">指定啟動診斷資料的本機路徑。</span><span class="sxs-lookup"><span data-stu-id="23d7c-120">Specifies the local path for the boot diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: LinuxParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d7c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="23d7c-121">-Name</span></span>
<span data-ttu-id="23d7c-122">指定此 Cmdlet 取得診斷資料之虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="23d7c-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d7c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23d7c-123">-ResourceGroupName</span></span>
<span data-ttu-id="23d7c-124">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="23d7c-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="23d7c-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="23d7c-125">-Windows</span></span>
<span data-ttu-id="23d7c-126">表示虛擬機器執行的是 Windows 作業系統。</span><span class="sxs-lookup"><span data-stu-id="23d7c-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d7c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d7c-127">CommonParameters</span></span>
<span data-ttu-id="23d7c-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23d7c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d7c-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="23d7c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d7c-130">輸入</span><span class="sxs-lookup"><span data-stu-id="23d7c-130">INPUTS</span></span>

### <span data-ttu-id="23d7c-131">所有</span><span class="sxs-lookup"><span data-stu-id="23d7c-131">None</span></span>
<span data-ttu-id="23d7c-132">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="23d7c-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="23d7c-133">輸出</span><span class="sxs-lookup"><span data-stu-id="23d7c-133">OUTPUTS</span></span>

### <span data-ttu-id="23d7c-134">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="23d7c-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="23d7c-135">PSVirtualMachineInstanceView 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="23d7c-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="23d7c-136">筆記</span><span class="sxs-lookup"><span data-stu-id="23d7c-136">NOTES</span></span>

## <span data-ttu-id="23d7c-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="23d7c-137">RELATED LINKS</span></span>

[<span data-ttu-id="23d7c-138">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="23d7c-138">Set-AzureRmVMBootDiagnostics</span></span>](./Set-AzureRmVMBootDiagnostics.md)

