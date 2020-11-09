---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: f198db6a49e1f5165dcfcd4effd91106cc0df831
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286759"
---
# <span data-ttu-id="bcd39-101">Get-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="bcd39-101">Get-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="bcd39-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bcd39-102">SYNOPSIS</span></span>
<span data-ttu-id="bcd39-103">取得與裝置上的儲存空間帳戶相對應的儲存空間帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="bcd39-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="bcd39-104">句法</span><span class="sxs-lookup"><span data-stu-id="bcd39-104">SYNTAX</span></span>

### <span data-ttu-id="bcd39-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bcd39-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcd39-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcd39-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bcd39-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcd39-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcd39-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcd39-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="bcd39-109">說明</span><span class="sxs-lookup"><span data-stu-id="bcd39-109">DESCRIPTION</span></span>
<span data-ttu-id="bcd39-110">**AzStackEdgeStorageAccountCredential** Cmdlet 會取得堆疊 Edge 裝置上對應之儲存空間帳戶的儲存空間帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="bcd39-110">The **Get-AzStackEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Stack Edge device.</span></span> <span data-ttu-id="bcd39-111">您可以指定名稱、資源群組名稱和裝置名稱參數，以取得特定儲存空間帳號憑證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bcd39-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="bcd39-112">示例</span><span class="sxs-lookup"><span data-stu-id="bcd39-112">EXAMPLES</span></span>

### <span data-ttu-id="bcd39-113">範例1</span><span class="sxs-lookup"><span data-stu-id="bcd39-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="bcd39-114">參數</span><span class="sxs-lookup"><span data-stu-id="bcd39-114">PARAMETERS</span></span>

### <span data-ttu-id="bcd39-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcd39-115">-DefaultProfile</span></span>
<span data-ttu-id="bcd39-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bcd39-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcd39-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="bcd39-117">-DeviceName</span></span>
<span data-ttu-id="bcd39-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="bcd39-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcd39-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="bcd39-119">-DeviceObject</span></span>
<span data-ttu-id="bcd39-120">請提供相對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="bcd39-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcd39-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="bcd39-121">-Name</span></span>
<span data-ttu-id="bcd39-122">要使用的儲存空間帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="bcd39-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: StorageAccountCredentialName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcd39-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcd39-123">-ResourceGroupName</span></span>
<span data-ttu-id="bcd39-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="bcd39-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcd39-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcd39-125">-ResourceId</span></span>
<span data-ttu-id="bcd39-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcd39-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="bcd39-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcd39-127">CommonParameters</span></span>
<span data-ttu-id="bcd39-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bcd39-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcd39-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bcd39-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcd39-130">輸入</span><span class="sxs-lookup"><span data-stu-id="bcd39-130">INPUTS</span></span>

### <span data-ttu-id="bcd39-131">PSStackEdgeDevice （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="bcd39-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="bcd39-132">輸出</span><span class="sxs-lookup"><span data-stu-id="bcd39-132">OUTPUTS</span></span>

### <span data-ttu-id="bcd39-133">PSStackEdgeStorageAccountCredential （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="bcd39-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="bcd39-134">筆記</span><span class="sxs-lookup"><span data-stu-id="bcd39-134">NOTES</span></span>

## <span data-ttu-id="bcd39-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="bcd39-135">RELATED LINKS</span></span>