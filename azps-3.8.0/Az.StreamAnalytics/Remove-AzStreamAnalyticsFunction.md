---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
ms.openlocfilehash: d481cf5ba28a87e098691d4b3fa5c179670d881d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798033"
---
# <span data-ttu-id="5ceac-101">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="5ceac-101">Remove-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="5ceac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ceac-102">SYNOPSIS</span></span>
<span data-ttu-id="5ceac-103">從資料流程分析作業中刪除函數。</span><span class="sxs-lookup"><span data-stu-id="5ceac-103">Deletes a function from a Stream Analytics job.</span></span>

## <span data-ttu-id="5ceac-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ceac-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ceac-105">說明</span><span class="sxs-lookup"><span data-stu-id="5ceac-105">DESCRIPTION</span></span>
<span data-ttu-id="5ceac-106">**AzStreamAnalyticsFunction** Cmdlet 會從 Azure Stream Analytics 作業非同步刪除函數。</span><span class="sxs-lookup"><span data-stu-id="5ceac-106">The **Remove-AzStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="5ceac-107">示例</span><span class="sxs-lookup"><span data-stu-id="5ceac-107">EXAMPLES</span></span>

### <span data-ttu-id="5ceac-108">範例1：移除資料流程分析函數</span><span class="sxs-lookup"><span data-stu-id="5ceac-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="5ceac-109">這個命令會從名為 StreamJob22 的作業中移除名為 ScoreTweet 的函數。</span><span class="sxs-lookup"><span data-stu-id="5ceac-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="5ceac-110">參數</span><span class="sxs-lookup"><span data-stu-id="5ceac-110">PARAMETERS</span></span>

### <span data-ttu-id="5ceac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ceac-111">-DefaultProfile</span></span>
<span data-ttu-id="5ceac-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ceac-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ceac-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="5ceac-113">-JobName</span></span>
<span data-ttu-id="5ceac-114">指定函數所屬的資料流程分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ceac-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="5ceac-115">這個 Cmdlet 會從此參數指定的作業中移除函數。</span><span class="sxs-lookup"><span data-stu-id="5ceac-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ceac-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="5ceac-116">-Name</span></span>
<span data-ttu-id="5ceac-117">指定此 Cmdlet 移除的資料流程分析函數的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ceac-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ceac-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ceac-118">-ResourceGroupName</span></span>
<span data-ttu-id="5ceac-119">指定 Stream Analytics 函數所歸屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ceac-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="5ceac-120">這個 Cmdlet 會刪除此參數指定之資源群組中的函數。</span><span class="sxs-lookup"><span data-stu-id="5ceac-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5ceac-121">-確認</span><span class="sxs-lookup"><span data-stu-id="5ceac-121">-Confirm</span></span>
<span data-ttu-id="5ceac-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5ceac-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ceac-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ceac-123">-WhatIf</span></span>
<span data-ttu-id="5ceac-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5ceac-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ceac-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5ceac-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ceac-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ceac-126">CommonParameters</span></span>
<span data-ttu-id="5ceac-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ceac-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ceac-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5ceac-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ceac-129">輸入</span><span class="sxs-lookup"><span data-stu-id="5ceac-129">INPUTS</span></span>

### <span data-ttu-id="5ceac-130">System.object</span><span class="sxs-lookup"><span data-stu-id="5ceac-130">System.String</span></span>

## <span data-ttu-id="5ceac-131">輸出</span><span class="sxs-lookup"><span data-stu-id="5ceac-131">OUTPUTS</span></span>

### <span data-ttu-id="5ceac-132">System.object</span><span class="sxs-lookup"><span data-stu-id="5ceac-132">System.Boolean</span></span>

## <span data-ttu-id="5ceac-133">筆記</span><span class="sxs-lookup"><span data-stu-id="5ceac-133">NOTES</span></span>

## <span data-ttu-id="5ceac-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ceac-134">RELATED LINKS</span></span>

[<span data-ttu-id="5ceac-135">AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="5ceac-135">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="5ceac-136">新-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="5ceac-136">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="5ceac-137">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="5ceac-137">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)

