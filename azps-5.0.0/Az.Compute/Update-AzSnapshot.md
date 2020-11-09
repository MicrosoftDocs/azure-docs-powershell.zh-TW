---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
ms.openlocfilehash: 6cfe2fd958d74740195b0bb29d3defa34f1310a2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284500"
---
# <span data-ttu-id="6da0e-101">Update-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="6da0e-101">Update-AzSnapshot</span></span>

## <span data-ttu-id="6da0e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6da0e-102">SYNOPSIS</span></span>
<span data-ttu-id="6da0e-103">更新快照。</span><span class="sxs-lookup"><span data-stu-id="6da0e-103">Updates a snapshot.</span></span>

## <span data-ttu-id="6da0e-104">句法</span><span class="sxs-lookup"><span data-stu-id="6da0e-104">SYNTAX</span></span>

### <span data-ttu-id="6da0e-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="6da0e-105">DefaultParameter (Default)</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-SnapshotUpdate] <PSSnapshotUpdate>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6da0e-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="6da0e-106">FriendMethod</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6da0e-107">說明</span><span class="sxs-lookup"><span data-stu-id="6da0e-107">DESCRIPTION</span></span>
<span data-ttu-id="6da0e-108">**AzSnapshot** Cmdlet 會更新快照。</span><span class="sxs-lookup"><span data-stu-id="6da0e-108">The **Update-AzSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="6da0e-109">示例</span><span class="sxs-lookup"><span data-stu-id="6da0e-109">EXAMPLES</span></span>

### <span data-ttu-id="6da0e-110">範例1</span><span class="sxs-lookup"><span data-stu-id="6da0e-110">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="6da0e-111">第一個命令會在 Premium_LRS 儲存帳戶類型中，建立一個大小為10GB 的本機空白快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="6da0e-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="6da0e-112">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="6da0e-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="6da0e-113">第二個和第三個命令會設定快照更新物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="6da0e-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="6da0e-114">最後一個命令會採用快照更新物件，並更新資源群組 "ResourceGroup01" 中名稱為 "Snapshot01" 的現有快照。</span><span class="sxs-lookup"><span data-stu-id="6da0e-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="6da0e-115">範例2</span><span class="sxs-lookup"><span data-stu-id="6da0e-115">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="6da0e-116">這個命令會將資源群組 ' ResourceGroup01 ' 中名稱為 ' Snapshot01 ' 的現有快照更新為 10 GB 磁片大小。</span><span class="sxs-lookup"><span data-stu-id="6da0e-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="6da0e-117">範例3</span><span class="sxs-lookup"><span data-stu-id="6da0e-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="6da0e-118">這些命令也會將資源群組 ' ResourceGroup01 ' 中名稱為 ' Snapshot01 ' 的現有快照更新為 10 GB 磁片大小。</span><span class="sxs-lookup"><span data-stu-id="6da0e-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="6da0e-119">參數</span><span class="sxs-lookup"><span data-stu-id="6da0e-119">PARAMETERS</span></span>

### <span data-ttu-id="6da0e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6da0e-120">-AsJob</span></span>
<span data-ttu-id="6da0e-121">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="6da0e-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6da0e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6da0e-122">-DefaultProfile</span></span>
<span data-ttu-id="6da0e-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6da0e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6da0e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6da0e-124">-ResourceGroupName</span></span>
<span data-ttu-id="6da0e-125">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6da0e-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6da0e-126">-快照</span><span class="sxs-lookup"><span data-stu-id="6da0e-126">-Snapshot</span></span>
<span data-ttu-id="6da0e-127">指定本機快照物件。</span><span class="sxs-lookup"><span data-stu-id="6da0e-127">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6da0e-128">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="6da0e-128">-SnapshotName</span></span>
<span data-ttu-id="6da0e-129">指定快照的名稱。</span><span class="sxs-lookup"><span data-stu-id="6da0e-129">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="6da0e-130">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="6da0e-130">-SnapshotUpdate</span></span>
<span data-ttu-id="6da0e-131">指定本機快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="6da0e-131">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6da0e-132">-確認</span><span class="sxs-lookup"><span data-stu-id="6da0e-132">-Confirm</span></span>
<span data-ttu-id="6da0e-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6da0e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6da0e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6da0e-134">-WhatIf</span></span>
<span data-ttu-id="6da0e-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6da0e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6da0e-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6da0e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6da0e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6da0e-137">CommonParameters</span></span>
<span data-ttu-id="6da0e-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6da0e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6da0e-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6da0e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6da0e-140">輸入</span><span class="sxs-lookup"><span data-stu-id="6da0e-140">INPUTS</span></span>

### <span data-ttu-id="6da0e-141">System.object</span><span class="sxs-lookup"><span data-stu-id="6da0e-141">System.String</span></span>

### <span data-ttu-id="6da0e-142">PSSnapshotUpdate 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="6da0e-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="6da0e-143">PSSnapshot 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="6da0e-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="6da0e-144">輸出</span><span class="sxs-lookup"><span data-stu-id="6da0e-144">OUTPUTS</span></span>

### <span data-ttu-id="6da0e-145">PSSnapshot 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="6da0e-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="6da0e-146">筆記</span><span class="sxs-lookup"><span data-stu-id="6da0e-146">NOTES</span></span>

## <span data-ttu-id="6da0e-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="6da0e-147">RELATED LINKS</span></span>