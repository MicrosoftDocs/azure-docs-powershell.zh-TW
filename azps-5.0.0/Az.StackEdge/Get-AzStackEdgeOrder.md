---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
ms.openlocfilehash: 2ef7b7ac2a06da0ef0f4b09d82f9a4ed447618ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286760"
---
# <span data-ttu-id="c0987-101">Get-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="c0987-101">Get-AzStackEdgeOrder</span></span>

## <span data-ttu-id="c0987-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0987-102">SYNOPSIS</span></span>
<span data-ttu-id="c0987-103">取得裝置的訂單詳細資料</span><span class="sxs-lookup"><span data-stu-id="c0987-103">Get the order details for a device</span></span>

## <span data-ttu-id="c0987-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0987-104">SYNTAX</span></span>

### <span data-ttu-id="c0987-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c0987-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0987-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0987-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzStackEdgeOrder -DeviceObject <PSStackEdgeOrder> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0987-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0987-107">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0987-108">說明</span><span class="sxs-lookup"><span data-stu-id="c0987-108">DESCRIPTION</span></span>
<span data-ttu-id="c0987-109">**AzStackEdgeOrder** Cmdlet 會取得堆疊 Edge 裝置的訂單詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c0987-109">The **Get-AzStackEdgeOrder** cmdlet gets the order details for a Stack Edge device.</span></span> 

## <span data-ttu-id="c0987-110">示例</span><span class="sxs-lookup"><span data-stu-id="c0987-110">EXAMPLES</span></span>

### <span data-ttu-id="c0987-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c0987-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="c0987-112">參數</span><span class="sxs-lookup"><span data-stu-id="c0987-112">PARAMETERS</span></span>

### <span data-ttu-id="c0987-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0987-113">-DefaultProfile</span></span>
<span data-ttu-id="c0987-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0987-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0987-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c0987-115">-DeviceName</span></span>
<span data-ttu-id="c0987-116">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="c0987-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0987-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="c0987-117">-DeviceObject</span></span>
<span data-ttu-id="c0987-118">請提供相對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="c0987-118">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder
Parameter Sets: GetByDeviceObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0987-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0987-119">-ResourceGroupName</span></span>
<span data-ttu-id="c0987-120">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="c0987-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0987-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0987-121">-ResourceId</span></span>
<span data-ttu-id="c0987-122">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0987-122">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0987-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0987-123">CommonParameters</span></span>
<span data-ttu-id="c0987-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0987-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0987-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c0987-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0987-126">輸入</span><span class="sxs-lookup"><span data-stu-id="c0987-126">INPUTS</span></span>

### <span data-ttu-id="c0987-127">PSStackEdgeDevice （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="c0987-127">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

### <span data-ttu-id="c0987-128">System.object</span><span class="sxs-lookup"><span data-stu-id="c0987-128">System.String</span></span>

## <span data-ttu-id="c0987-129">輸出</span><span class="sxs-lookup"><span data-stu-id="c0987-129">OUTPUTS</span></span>

### <span data-ttu-id="c0987-130">PSStackEdgeOrder （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="c0987-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="c0987-131">筆記</span><span class="sxs-lookup"><span data-stu-id="c0987-131">NOTES</span></span>

## <span data-ttu-id="c0987-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0987-132">RELATED LINKS</span></span>