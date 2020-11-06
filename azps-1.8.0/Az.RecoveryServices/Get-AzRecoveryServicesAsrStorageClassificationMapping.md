---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: a341e634c9c426843b5eb217c2f13102abc30ae4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621164"
---
# <span data-ttu-id="a3a10-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="a3a10-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="a3a10-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a3a10-102">SYNOPSIS</span></span>
<span data-ttu-id="a3a10-103">取得 ASR 儲存分類對應。</span><span class="sxs-lookup"><span data-stu-id="a3a10-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="a3a10-104">句法</span><span class="sxs-lookup"><span data-stu-id="a3a10-104">SYNTAX</span></span>

### <span data-ttu-id="a3a10-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="a3a10-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3a10-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="a3a10-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3a10-107">說明</span><span class="sxs-lookup"><span data-stu-id="a3a10-107">DESCRIPTION</span></span>
<span data-ttu-id="a3a10-108">**AzRecoveryServicesAsrStorageClassificationMapping** Cmdlet 會取得 ASR 儲存分類對應的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a3a10-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="a3a10-109">示例</span><span class="sxs-lookup"><span data-stu-id="a3a10-109">EXAMPLES</span></span>

### <span data-ttu-id="a3a10-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a3a10-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="a3a10-111">列出與指定的儲存分類相關的所有儲存分類對應。</span><span class="sxs-lookup"><span data-stu-id="a3a10-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="a3a10-112">參數</span><span class="sxs-lookup"><span data-stu-id="a3a10-112">PARAMETERS</span></span>

### <span data-ttu-id="a3a10-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3a10-113">-DefaultProfile</span></span>
<span data-ttu-id="a3a10-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a3a10-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a3a10-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="a3a10-115">-Name</span></span>
<span data-ttu-id="a3a10-116">指定要取得之儲存分類對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3a10-116">Specifies the name of the storage classification mapping to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3a10-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="a3a10-117">-StorageClassification</span></span>
<span data-ttu-id="a3a10-118">指定 ASR 儲存分類物件。</span><span class="sxs-lookup"><span data-stu-id="a3a10-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="a3a10-119">這個 Cmdlet 會取得與指定的儲存分類相對應的 ASR 儲存分類對應</span><span class="sxs-lookup"><span data-stu-id="a3a10-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3a10-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3a10-120">CommonParameters</span></span>
<span data-ttu-id="a3a10-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a3a10-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3a10-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a3a10-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3a10-123">輸入</span><span class="sxs-lookup"><span data-stu-id="a3a10-123">INPUTS</span></span>

### <span data-ttu-id="a3a10-124">RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="a3a10-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="a3a10-125">輸出</span><span class="sxs-lookup"><span data-stu-id="a3a10-125">OUTPUTS</span></span>

### <span data-ttu-id="a3a10-126">RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="a3a10-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="a3a10-127">筆記</span><span class="sxs-lookup"><span data-stu-id="a3a10-127">NOTES</span></span>

## <span data-ttu-id="a3a10-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3a10-128">RELATED LINKS</span></span>

[<span data-ttu-id="a3a10-129">新-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="a3a10-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="a3a10-130">移除-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="a3a10-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)