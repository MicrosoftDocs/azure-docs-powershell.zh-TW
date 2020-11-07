---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
ms.openlocfilehash: a431428c670dba7e0bfb152bde0cae22f47d8099
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957509"
---
# <span data-ttu-id="97749-101">Grant-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="97749-101">Grant-AzSnapshotAccess</span></span>

## <span data-ttu-id="97749-102">摘要</span><span class="sxs-lookup"><span data-stu-id="97749-102">SYNOPSIS</span></span>
<span data-ttu-id="97749-103">授與快照存取權。</span><span class="sxs-lookup"><span data-stu-id="97749-103">Grants an access to a snapshot.</span></span>

## <span data-ttu-id="97749-104">句法</span><span class="sxs-lookup"><span data-stu-id="97749-104">SYNTAX</span></span>

```
Grant-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97749-105">說明</span><span class="sxs-lookup"><span data-stu-id="97749-105">DESCRIPTION</span></span>
<span data-ttu-id="97749-106">**Grant AzSnapshotAccess** Cmdlet 會授權存取快照。</span><span class="sxs-lookup"><span data-stu-id="97749-106">The **Grant-AzSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="97749-107">示例</span><span class="sxs-lookup"><span data-stu-id="97749-107">EXAMPLES</span></span>

### <span data-ttu-id="97749-108">範例1</span><span class="sxs-lookup"><span data-stu-id="97749-108">Example 1</span></span>
```
PS C:\> Grant-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="97749-109">針對60秒的資源群組中名為「Snapshot01」的快照，授與「Read」的存取權。</span><span class="sxs-lookup"><span data-stu-id="97749-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="97749-110">參數</span><span class="sxs-lookup"><span data-stu-id="97749-110">PARAMETERS</span></span>

### <span data-ttu-id="97749-111">-Access</span><span class="sxs-lookup"><span data-stu-id="97749-111">-Access</span></span>
<span data-ttu-id="97749-112">指定存取層級。</span><span class="sxs-lookup"><span data-stu-id="97749-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97749-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97749-113">-AsJob</span></span>
<span data-ttu-id="97749-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="97749-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97749-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97749-115">-DefaultProfile</span></span>
<span data-ttu-id="97749-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="97749-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97749-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="97749-117">-DurationInSecond</span></span>
<span data-ttu-id="97749-118">指定存取持續時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="97749-118">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97749-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97749-119">-ResourceGroupName</span></span>
<span data-ttu-id="97749-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="97749-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="97749-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="97749-121">-SnapshotName</span></span>
<span data-ttu-id="97749-122">指定快照的名稱。</span><span class="sxs-lookup"><span data-stu-id="97749-122">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="97749-123">-確認</span><span class="sxs-lookup"><span data-stu-id="97749-123">-Confirm</span></span>
<span data-ttu-id="97749-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="97749-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97749-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97749-125">-WhatIf</span></span>
<span data-ttu-id="97749-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="97749-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97749-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="97749-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97749-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97749-128">CommonParameters</span></span>
<span data-ttu-id="97749-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="97749-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97749-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="97749-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97749-131">輸入</span><span class="sxs-lookup"><span data-stu-id="97749-131">INPUTS</span></span>

### <span data-ttu-id="97749-132">System.object</span><span class="sxs-lookup"><span data-stu-id="97749-132">System.String</span></span>

## <span data-ttu-id="97749-133">輸出</span><span class="sxs-lookup"><span data-stu-id="97749-133">OUTPUTS</span></span>

### <span data-ttu-id="97749-134">PSAccessUri 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="97749-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="97749-135">筆記</span><span class="sxs-lookup"><span data-stu-id="97749-135">NOTES</span></span>

## <span data-ttu-id="97749-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="97749-136">RELATED LINKS</span></span>