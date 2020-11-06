---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 9FD4DB8C-B242-4F9A-92E5-0B3EDED00521
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoStartPolicy.md
ms.openlocfilehash: 449206713291499c344975e490c3b0d89ab1d88a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622395"
---
# <span data-ttu-id="5089d-101">Get-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="5089d-101">Get-AzDtlAutoStartPolicy</span></span>

## <span data-ttu-id="5089d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5089d-102">SYNOPSIS</span></span>
<span data-ttu-id="5089d-103">在 DevTest Labs 中取得 lab 的自動啟動原則。</span><span class="sxs-lookup"><span data-stu-id="5089d-103">Gets the auto start policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="5089d-104">句法</span><span class="sxs-lookup"><span data-stu-id="5089d-104">SYNTAX</span></span>

```
Get-AzDtlAutoStartPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5089d-105">說明</span><span class="sxs-lookup"><span data-stu-id="5089d-105">DESCRIPTION</span></span>
<span data-ttu-id="5089d-106">**AzDtlAutoStartPolicy** Cmdlet 會取得 lab 的自動啟動原則，此原則會安排自動啟動的實驗室虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5089d-106">The **Get-AzDtlAutoStartPolicy** cmdlet gets the auto start policy of a lab which schedules lab virtual machines for automatic start.</span></span>
<span data-ttu-id="5089d-107">這個 Cmdlet 會傳回原則的啟用或停用狀態，以及一周的天數，以及一天的時間，以及您已設定為允許將實驗室虛擬機器自動啟動的時間。</span><span class="sxs-lookup"><span data-stu-id="5089d-107">The cmdlet returns the enabled or disabled status of the policy and the days of the week and time of day that you have set to allow lab virtual machines to be scheduled for automatic start.</span></span>

## <span data-ttu-id="5089d-108">示例</span><span class="sxs-lookup"><span data-stu-id="5089d-108">EXAMPLES</span></span>

## <span data-ttu-id="5089d-109">參數</span><span class="sxs-lookup"><span data-stu-id="5089d-109">PARAMETERS</span></span>

### <span data-ttu-id="5089d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5089d-110">-DefaultProfile</span></span>
<span data-ttu-id="5089d-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5089d-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5089d-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="5089d-112">-LabName</span></span>
<span data-ttu-id="5089d-113">指定此 Cmdlet 取得自動啟動原則的實驗名稱。</span><span class="sxs-lookup"><span data-stu-id="5089d-113">Specifies the name of the lab for which this cmdlet gets the auto start policy.</span></span>

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

### <span data-ttu-id="5089d-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5089d-114">-ResourceGroupName</span></span>
<span data-ttu-id="5089d-115">指定實驗室所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5089d-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="5089d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5089d-116">CommonParameters</span></span>
<span data-ttu-id="5089d-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5089d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5089d-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5089d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5089d-119">輸入</span><span class="sxs-lookup"><span data-stu-id="5089d-119">INPUTS</span></span>

### <span data-ttu-id="5089d-120">System.object</span><span class="sxs-lookup"><span data-stu-id="5089d-120">System.String</span></span>

## <span data-ttu-id="5089d-121">輸出</span><span class="sxs-lookup"><span data-stu-id="5089d-121">OUTPUTS</span></span>

### <span data-ttu-id="5089d-122">PSSchedule 中的 DevTestLabs。</span><span class="sxs-lookup"><span data-stu-id="5089d-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="5089d-123">筆記</span><span class="sxs-lookup"><span data-stu-id="5089d-123">NOTES</span></span>

## <span data-ttu-id="5089d-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="5089d-124">RELATED LINKS</span></span>

[<span data-ttu-id="5089d-125">Set-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="5089d-125">Set-AzDtlAutoStartPolicy</span></span>](./Set-AzDtlAutoStartPolicy.md)

