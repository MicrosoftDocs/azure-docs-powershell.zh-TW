---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: 3ab0dc0acb02d2efa9f7da29dd096ad03f1eb57e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286616"
---
# <span data-ttu-id="a408c-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="a408c-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="a408c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a408c-102">SYNOPSIS</span></span>
<span data-ttu-id="a408c-103">顯示最新的「虛擬機器規模設定」輪流升級的狀態。</span><span class="sxs-lookup"><span data-stu-id="a408c-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="a408c-104">句法</span><span class="sxs-lookup"><span data-stu-id="a408c-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a408c-105">說明</span><span class="sxs-lookup"><span data-stu-id="a408c-105">DESCRIPTION</span></span>
<span data-ttu-id="a408c-106">顯示最新的「虛擬機器規模設定」輪流升級的狀態。</span><span class="sxs-lookup"><span data-stu-id="a408c-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="a408c-107">示例</span><span class="sxs-lookup"><span data-stu-id="a408c-107">EXAMPLES</span></span>

### <span data-ttu-id="a408c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a408c-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="a408c-109">這個命令會顯示屬於名為 Group001 之資源群組之名為 VMSS001 之 VMSS 的最新輪流升級狀態。</span><span class="sxs-lookup"><span data-stu-id="a408c-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="a408c-110">參數</span><span class="sxs-lookup"><span data-stu-id="a408c-110">PARAMETERS</span></span>

### <span data-ttu-id="a408c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a408c-111">-DefaultProfile</span></span>
<span data-ttu-id="a408c-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a408c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a408c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a408c-113">-ResourceGroupName</span></span>
<span data-ttu-id="a408c-114">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a408c-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="a408c-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a408c-115">-VMScaleSetName</span></span>
<span data-ttu-id="a408c-116">VM 比例集的名稱。</span><span class="sxs-lookup"><span data-stu-id="a408c-116">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a408c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a408c-117">CommonParameters</span></span>
<span data-ttu-id="a408c-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a408c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a408c-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a408c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a408c-120">輸入</span><span class="sxs-lookup"><span data-stu-id="a408c-120">INPUTS</span></span>

### <span data-ttu-id="a408c-121">System.object</span><span class="sxs-lookup"><span data-stu-id="a408c-121">System.String</span></span>

## <span data-ttu-id="a408c-122">輸出</span><span class="sxs-lookup"><span data-stu-id="a408c-122">OUTPUTS</span></span>

### <span data-ttu-id="a408c-123">PSRollingUpgradeStatusInfo 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="a408c-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="a408c-124">筆記</span><span class="sxs-lookup"><span data-stu-id="a408c-124">NOTES</span></span>

## <span data-ttu-id="a408c-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="a408c-125">RELATED LINKS</span></span>