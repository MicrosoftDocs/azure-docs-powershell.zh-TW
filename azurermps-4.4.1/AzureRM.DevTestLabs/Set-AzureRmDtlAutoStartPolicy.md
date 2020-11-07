---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 3FADEC2E-4A2B-46EB-8A94-CF48D717C7FC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: a1efa9159bbe318a1de0360a3f70f197660db535
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625181"
---
# <span data-ttu-id="ead33-101">Set-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="ead33-101">Set-AzureRmDtlAutoStartPolicy</span></span>

## <span data-ttu-id="ead33-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ead33-102">SYNOPSIS</span></span>
<span data-ttu-id="ead33-103">在 DevTest Labs 中設定實驗的自動啟動原則。</span><span class="sxs-lookup"><span data-stu-id="ead33-103">Sets the auto start policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ead33-104">句法</span><span class="sxs-lookup"><span data-stu-id="ead33-104">SYNTAX</span></span>

### <span data-ttu-id="ead33-105">啟用 (預設) </span><span class="sxs-lookup"><span data-stu-id="ead33-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ead33-106">禁止</span><span class="sxs-lookup"><span data-stu-id="ead33-106">Disable</span></span>
```
Set-AzureRmDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ead33-107">說明</span><span class="sxs-lookup"><span data-stu-id="ead33-107">DESCRIPTION</span></span>
<span data-ttu-id="ead33-108">**AzureRmDtlAutoStartPolicy** Cmdlet 會設定 lab 的自動啟動原則，這可讓實驗式虛擬機器排程自動啟動。</span><span class="sxs-lookup"><span data-stu-id="ead33-108">The **Set-AzureRmDtlAutoStartPolicy** cmdlet sets the auto start policy of a lab, which allows lab virtual machines to be scheduled for automatic start.</span></span>
<span data-ttu-id="ead33-109">此 Cmdlet 會使用指定的資源群組和 lab 名稱來設定原則。</span><span class="sxs-lookup"><span data-stu-id="ead33-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="ead33-110">示例</span><span class="sxs-lookup"><span data-stu-id="ead33-110">EXAMPLES</span></span>

## <span data-ttu-id="ead33-111">參數</span><span class="sxs-lookup"><span data-stu-id="ead33-111">PARAMETERS</span></span>

### <span data-ttu-id="ead33-112">天</span><span class="sxs-lookup"><span data-stu-id="ead33-112">-Days</span></span>
<span data-ttu-id="ead33-113">指定為數組，即必須在每週的哪幾天啟動實驗室的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ead33-113">Specifies, as an array, the days of the week for when the virtual machines of the lab must be started.</span></span>

```yaml
Type: System.DayOfWeek[]
Parameter Sets: (All)
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ead33-114">-停用</span><span class="sxs-lookup"><span data-stu-id="ead33-114">-Disable</span></span>
<span data-ttu-id="ead33-115">表示此 Cmdlet 會針對實驗室中的虛擬機器停用原則。</span><span class="sxs-lookup"><span data-stu-id="ead33-115">Indicates that this cmdlet disables the policy for the virtual machines in the lab.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ead33-116">-啟用</span><span class="sxs-lookup"><span data-stu-id="ead33-116">-Enable</span></span>
<span data-ttu-id="ead33-117">表示此 Cmdlet 會針對實驗室中的虛擬機器啟用原則。</span><span class="sxs-lookup"><span data-stu-id="ead33-117">Indicates that this cmdlet enables the policy for the virtual machines in the lab.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ead33-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="ead33-118">-LabName</span></span>
<span data-ttu-id="ead33-119">指定此 Cmdlet 設定自動啟動原則的實驗名稱。</span><span class="sxs-lookup"><span data-stu-id="ead33-119">Specifies the name of the lab for which this cmdlet sets the automatic start policy.</span></span>

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

### <span data-ttu-id="ead33-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ead33-120">-ResourceGroupName</span></span>
<span data-ttu-id="ead33-121">指定實驗室所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ead33-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="ead33-122">時間</span><span class="sxs-lookup"><span data-stu-id="ead33-122">-Time</span></span>
<span data-ttu-id="ead33-123">指定實驗室的虛擬機器必須開始的時間。</span><span class="sxs-lookup"><span data-stu-id="ead33-123">Specifies the time when the virtual machines of the lab must be started.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ead33-124">-確認</span><span class="sxs-lookup"><span data-stu-id="ead33-124">-Confirm</span></span>
<span data-ttu-id="ead33-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ead33-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ead33-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ead33-126">-WhatIf</span></span>
<span data-ttu-id="ead33-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ead33-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ead33-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ead33-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ead33-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ead33-129">-DefaultProfile</span></span>
<span data-ttu-id="ead33-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ead33-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ead33-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ead33-131">CommonParameters</span></span>
<span data-ttu-id="ead33-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ead33-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ead33-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ead33-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ead33-134">輸入</span><span class="sxs-lookup"><span data-stu-id="ead33-134">INPUTS</span></span>

## <span data-ttu-id="ead33-135">輸出</span><span class="sxs-lookup"><span data-stu-id="ead33-135">OUTPUTS</span></span>

### <span data-ttu-id="ead33-136">PSSchedule 中的 DevTestLabs。</span><span class="sxs-lookup"><span data-stu-id="ead33-136">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="ead33-137">這個 Cmdlet 會傳回排程，以指定實驗室的虛擬機器必須何時啟動。</span><span class="sxs-lookup"><span data-stu-id="ead33-137">This cmdlet returns the schedule that specifies when the virtual machines of the lab must be started.</span></span>

## <span data-ttu-id="ead33-138">筆記</span><span class="sxs-lookup"><span data-stu-id="ead33-138">NOTES</span></span>

## <span data-ttu-id="ead33-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="ead33-139">RELATED LINKS</span></span>

[<span data-ttu-id="ead33-140">AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="ead33-140">Get-AzureRmDtlAutoStartPolicy</span></span>](./Get-AzureRmDtlAutoStartPolicy.md)

