---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
ms.openlocfilehash: cafc38503bd7978d1214fe8f3c78e4fd1f4a3e7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787502"
---
# <span data-ttu-id="fe7b0-101">Remove-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="fe7b0-101">Remove-AzIotHubCertificate</span></span>

## <span data-ttu-id="fe7b0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe7b0-102">SYNOPSIS</span></span>
<span data-ttu-id="fe7b0-103">刪除 Azure IoT 中樞憑證。</span><span class="sxs-lookup"><span data-stu-id="fe7b0-103">Deletes an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="fe7b0-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe7b0-104">SYNTAX</span></span>

### <span data-ttu-id="fe7b0-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fe7b0-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe7b0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fe7b0-106">InputObjectSet</span></span>
```
Remove-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe7b0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fe7b0-107">ResourceIdSet</span></span>
```
Remove-AzIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe7b0-108">說明</span><span class="sxs-lookup"><span data-stu-id="fe7b0-108">DESCRIPTION</span></span>
<span data-ttu-id="fe7b0-109">如需 Azure IoT 中樞中 CA 憑證的詳細說明，請參閱 https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="fe7b0-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="fe7b0-110">示例</span><span class="sxs-lookup"><span data-stu-id="fe7b0-110">EXAMPLES</span></span>

### <span data-ttu-id="fe7b0-111">範例1</span><span class="sxs-lookup"><span data-stu-id="fe7b0-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="fe7b0-112">刪除 MyCertificate</span><span class="sxs-lookup"><span data-stu-id="fe7b0-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="fe7b0-113">參數</span><span class="sxs-lookup"><span data-stu-id="fe7b0-113">PARAMETERS</span></span>

### <span data-ttu-id="fe7b0-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="fe7b0-114">-CertificateName</span></span>
<span data-ttu-id="fe7b0-115">憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="fe7b0-115">Name of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe7b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe7b0-116">-DefaultProfile</span></span>
<span data-ttu-id="fe7b0-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe7b0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe7b0-118">-Etag</span><span class="sxs-lookup"><span data-stu-id="fe7b0-118">-Etag</span></span>
<span data-ttu-id="fe7b0-119">憑證的 Etag</span><span class="sxs-lookup"><span data-stu-id="fe7b0-119">Etag of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe7b0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe7b0-120">-InputObject</span></span>
<span data-ttu-id="fe7b0-121">憑證物件</span><span class="sxs-lookup"><span data-stu-id="fe7b0-121">Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe7b0-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="fe7b0-122">-Name</span></span>
<span data-ttu-id="fe7b0-123">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="fe7b0-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe7b0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe7b0-124">-PassThru</span></span>
<span data-ttu-id="fe7b0-125">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="fe7b0-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="fe7b0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe7b0-126">-ResourceGroupName</span></span>
<span data-ttu-id="fe7b0-127">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="fe7b0-127">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe7b0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe7b0-128">-ResourceId</span></span>
<span data-ttu-id="fe7b0-129">憑證資源識別碼</span><span class="sxs-lookup"><span data-stu-id="fe7b0-129">Certificate Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe7b0-130">-確認</span><span class="sxs-lookup"><span data-stu-id="fe7b0-130">-Confirm</span></span>
<span data-ttu-id="fe7b0-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fe7b0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe7b0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe7b0-132">-WhatIf</span></span>
<span data-ttu-id="fe7b0-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fe7b0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe7b0-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fe7b0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe7b0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe7b0-135">CommonParameters</span></span>
<span data-ttu-id="fe7b0-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe7b0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe7b0-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fe7b0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe7b0-138">輸入</span><span class="sxs-lookup"><span data-stu-id="fe7b0-138">INPUTS</span></span>

### <span data-ttu-id="fe7b0-139">PSCertificateDescription （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="fe7b0-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="fe7b0-140">System.object</span><span class="sxs-lookup"><span data-stu-id="fe7b0-140">System.String</span></span>

## <span data-ttu-id="fe7b0-141">輸出</span><span class="sxs-lookup"><span data-stu-id="fe7b0-141">OUTPUTS</span></span>

### <span data-ttu-id="fe7b0-142">System.object</span><span class="sxs-lookup"><span data-stu-id="fe7b0-142">System.Boolean</span></span>

## <span data-ttu-id="fe7b0-143">筆記</span><span class="sxs-lookup"><span data-stu-id="fe7b0-143">NOTES</span></span>

## <span data-ttu-id="fe7b0-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe7b0-144">RELATED LINKS</span></span>