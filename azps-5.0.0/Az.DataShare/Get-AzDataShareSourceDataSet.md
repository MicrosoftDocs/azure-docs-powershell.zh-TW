---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesourcedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
ms.openlocfilehash: 5f10289a5890ffa0e2764c475d65a0d5103b705e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284914"
---
# <span data-ttu-id="0b603-101">Get-AzDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="0b603-101">Get-AzDataShareSourceDataSet</span></span>

## <span data-ttu-id="0b603-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b603-102">SYNOPSIS</span></span>
<span data-ttu-id="0b603-103">取得共用訂閱中源資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0b603-103">Gets information about source data sets in share subscription.</span></span>

## <span data-ttu-id="0b603-104">句法</span><span class="sxs-lookup"><span data-stu-id="0b603-104">SYNTAX</span></span>

### <span data-ttu-id="0b603-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0b603-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSourceDataSet -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b603-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b603-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSourceDataSet -ShareSubscriptionResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b603-107">說明</span><span class="sxs-lookup"><span data-stu-id="0b603-107">DESCRIPTION</span></span>
<span data-ttu-id="0b603-108">**AzDataShareSourceDataSet** Cmdlet 會提供共用訂閱中源資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0b603-108">The **Get-AzDataShareSourceDataSet** cmdlet provides information about the source data sets in the share subscription.</span></span> 

## <span data-ttu-id="0b603-109">示例</span><span class="sxs-lookup"><span data-stu-id="0b603-109">EXAMPLES</span></span>

### <span data-ttu-id="0b603-110">範例1</span><span class="sxs-lookup"><span data-stu-id="0b603-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSourceDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription"

DataSetId   : 63116d3f-515a-47a2-9b18-d981b16a9d21
DataSetName : filesystem1
DataSetType : Blob
Id          : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/consumerSourceDataSets/AdsDataSets
Name        : AdsDataSets
Type        : Microsoft.DataShare/ConsumerSourceDataSet
```

<span data-ttu-id="0b603-111">取得來源共用中可用的資料集</span><span class="sxs-lookup"><span data-stu-id="0b603-111">Gets datasets available in the source share</span></span>

## <span data-ttu-id="0b603-112">參數</span><span class="sxs-lookup"><span data-stu-id="0b603-112">PARAMETERS</span></span>

### <span data-ttu-id="0b603-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0b603-113">-AccountName</span></span>
<span data-ttu-id="0b603-114">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="0b603-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b603-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b603-115">-DefaultProfile</span></span>
<span data-ttu-id="0b603-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0b603-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b603-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b603-117">-ResourceGroupName</span></span>
<span data-ttu-id="0b603-118">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="0b603-118">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b603-119">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="0b603-119">-ShareSubscriptionName</span></span>
<span data-ttu-id="0b603-120">Azure 資料共用訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="0b603-120">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b603-121">-ShareSubscriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="0b603-121">-ShareSubscriptionResourceId</span></span>
<span data-ttu-id="0b603-122">Azure 資料共用訂閱資源識別碼</span><span class="sxs-lookup"><span data-stu-id="0b603-122">Azure data share subscription resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b603-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b603-123">CommonParameters</span></span>
<span data-ttu-id="0b603-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b603-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b603-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0b603-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b603-126">輸入</span><span class="sxs-lookup"><span data-stu-id="0b603-126">INPUTS</span></span>

### <span data-ttu-id="0b603-127">System.object</span><span class="sxs-lookup"><span data-stu-id="0b603-127">System.String</span></span>

## <span data-ttu-id="0b603-128">輸出</span><span class="sxs-lookup"><span data-stu-id="0b603-128">OUTPUTS</span></span>

### <span data-ttu-id="0b603-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="0b603-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span></span>

## <span data-ttu-id="0b603-130">筆記</span><span class="sxs-lookup"><span data-stu-id="0b603-130">NOTES</span></span>

## <span data-ttu-id="0b603-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b603-131">RELATED LINKS</span></span>