---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: 6ea65189969e38359bb6d4345ea4c47963f9eddf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274047"
---
# <span data-ttu-id="cb025-101">Remove-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="cb025-101">Remove-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="cb025-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb025-102">SYNOPSIS</span></span>
<span data-ttu-id="cb025-103">刪除 (ANF) 快照原則的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="cb025-103">Deletes an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="cb025-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb025-104">SYNTAX</span></span>

### <span data-ttu-id="cb025-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cb025-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb025-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb025-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb025-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb025-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb025-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb025-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -InputObject <PSNetAppFilesSnapshotPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb025-109">說明</span><span class="sxs-lookup"><span data-stu-id="cb025-109">DESCRIPTION</span></span>
<span data-ttu-id="cb025-110">**AzNetAppFilesSnapshotPolicy** Cmdlet 會刪除 ANF 快照原則。</span><span class="sxs-lookup"><span data-stu-id="cb025-110">The **Remove-AzNetAppFilesSnapshotPolicy** cmdlet deletes an ANF snapshot policy.</span></span>

## <span data-ttu-id="cb025-111">示例</span><span class="sxs-lookup"><span data-stu-id="cb025-111">EXAMPLES</span></span>

### <span data-ttu-id="cb025-112">範例1</span><span class="sxs-lookup"><span data-stu-id="cb025-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="cb025-113">這個命令會刪除帳戶 "我的帳戶" 的名稱為 "MyBackupPolicy" 的新 ANF 備份原則。</span><span class="sxs-lookup"><span data-stu-id="cb025-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="cb025-114">參數</span><span class="sxs-lookup"><span data-stu-id="cb025-114">PARAMETERS</span></span>

### <span data-ttu-id="cb025-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cb025-115">-AccountName</span></span>
<span data-ttu-id="cb025-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="cb025-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="cb025-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="cb025-117">-AccountObject</span></span>
<span data-ttu-id="cb025-118">新快照原則物件的帳戶</span><span class="sxs-lookup"><span data-stu-id="cb025-118">The Account for the new Snapshot Policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb025-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb025-119">-DefaultProfile</span></span>
<span data-ttu-id="cb025-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb025-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb025-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb025-121">-InputObject</span></span>
<span data-ttu-id="cb025-122">要移除的 SnapshotPolicy 物件</span><span class="sxs-lookup"><span data-stu-id="cb025-122">The SnapshotPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb025-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="cb025-123">-Name</span></span>
<span data-ttu-id="cb025-124">ANF 快照原則的名稱</span><span class="sxs-lookup"><span data-stu-id="cb025-124">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb025-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb025-125">-PassThru</span></span>
<span data-ttu-id="cb025-126">返回是否已成功移除指定的帳號</span><span class="sxs-lookup"><span data-stu-id="cb025-126">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="cb025-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb025-127">-ResourceGroupName</span></span>
<span data-ttu-id="cb025-128">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="cb025-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="cb025-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb025-129">-ResourceId</span></span>
<span data-ttu-id="cb025-130">ANF 快照原則的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="cb025-130">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="cb025-131">-確認</span><span class="sxs-lookup"><span data-stu-id="cb025-131">-Confirm</span></span>
<span data-ttu-id="cb025-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cb025-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb025-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb025-133">-WhatIf</span></span>
<span data-ttu-id="cb025-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cb025-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb025-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb025-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb025-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb025-136">CommonParameters</span></span>
<span data-ttu-id="cb025-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb025-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb025-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cb025-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb025-139">輸入</span><span class="sxs-lookup"><span data-stu-id="cb025-139">INPUTS</span></span>

### <span data-ttu-id="cb025-140">System.object</span><span class="sxs-lookup"><span data-stu-id="cb025-140">System.String</span></span>

### <span data-ttu-id="cb025-141">PSNetAppFilesAccount 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="cb025-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="cb025-142">PSNetAppFilesSnapshotPolicy 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="cb025-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="cb025-143">輸出</span><span class="sxs-lookup"><span data-stu-id="cb025-143">OUTPUTS</span></span>

### <span data-ttu-id="cb025-144">PSNetAppFilesSnapshotPolicy 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="cb025-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="cb025-145">筆記</span><span class="sxs-lookup"><span data-stu-id="cb025-145">NOTES</span></span>

## <span data-ttu-id="cb025-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb025-146">RELATED LINKS</span></span>