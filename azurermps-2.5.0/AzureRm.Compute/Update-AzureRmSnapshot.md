---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermsnapshot
schema: 2.0.0
ms.openlocfilehash: 2e8b538e9a6f5f9fce2fb768bc0c77d0c82c55f0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802513"
---
# <span data-ttu-id="5b717-101">Update-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="5b717-101">Update-AzureRmSnapshot</span></span>

## <span data-ttu-id="5b717-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5b717-102">SYNOPSIS</span></span>
<span data-ttu-id="5b717-103">更新快照。</span><span class="sxs-lookup"><span data-stu-id="5b717-103">Updates a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b717-104">句法</span><span class="sxs-lookup"><span data-stu-id="5b717-104">SYNTAX</span></span>

### <span data-ttu-id="5b717-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="5b717-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String>
 [-SnapshotUpdate] <PSSnapshotUpdate> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b717-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="5b717-106">FriendMethod</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b717-107">說明</span><span class="sxs-lookup"><span data-stu-id="5b717-107">DESCRIPTION</span></span>
<span data-ttu-id="5b717-108">**AzureRmSnapshot** Cmdlet 會更新快照。</span><span class="sxs-lookup"><span data-stu-id="5b717-108">The **Update-AzureRmSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="5b717-109">示例</span><span class="sxs-lookup"><span data-stu-id="5b717-109">EXAMPLES</span></span>

### <span data-ttu-id="5b717-110">範例1</span><span class="sxs-lookup"><span data-stu-id="5b717-110">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="5b717-111">第一個命令會在 Premium_LRS 儲存帳戶類型中，建立一個大小為10GB 的本機空白快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="5b717-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="5b717-112">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="5b717-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="5b717-113">第二個和第三個命令會設定快照更新物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="5b717-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="5b717-114">最後一個命令會採用快照更新物件，並更新資源群組 "ResourceGroup01" 中名稱為 "Snapshot01" 的現有快照。</span><span class="sxs-lookup"><span data-stu-id="5b717-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="5b717-115">範例2</span><span class="sxs-lookup"><span data-stu-id="5b717-115">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="5b717-116">這個命令會將資源群組 ' ResourceGroup01 ' 中名稱為 ' Snapshot01 ' 的現有快照更新為 10 GB 磁片大小。</span><span class="sxs-lookup"><span data-stu-id="5b717-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="5b717-117">範例3</span><span class="sxs-lookup"><span data-stu-id="5b717-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="5b717-118">這些命令也會將資源群組 ' ResourceGroup01 ' 中名稱為 ' Snapshot01 ' 的現有快照更新為 10 GB 磁片大小。</span><span class="sxs-lookup"><span data-stu-id="5b717-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="5b717-119">參數</span><span class="sxs-lookup"><span data-stu-id="5b717-119">PARAMETERS</span></span>

### <span data-ttu-id="5b717-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b717-120">-AsJob</span></span>
<span data-ttu-id="5b717-121">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="5b717-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b717-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b717-122">-DefaultProfile</span></span>
<span data-ttu-id="5b717-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b717-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b717-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b717-124">-ResourceGroupName</span></span>
<span data-ttu-id="5b717-125">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b717-125">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b717-126">-快照</span><span class="sxs-lookup"><span data-stu-id="5b717-126">-Snapshot</span></span>
<span data-ttu-id="5b717-127">指定本機快照物件。</span><span class="sxs-lookup"><span data-stu-id="5b717-127">Specifies a local snapshot object.</span></span>

```yaml
Type: PSSnapshot
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b717-128">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="5b717-128">-SnapshotName</span></span>
<span data-ttu-id="5b717-129">指定快照的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b717-129">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b717-130">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="5b717-130">-SnapshotUpdate</span></span>
<span data-ttu-id="5b717-131">指定本機快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="5b717-131">Specifies a local snapshot update object.</span></span>

```yaml
Type: PSSnapshotUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b717-132">-確認</span><span class="sxs-lookup"><span data-stu-id="5b717-132">-Confirm</span></span>
<span data-ttu-id="5b717-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5b717-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b717-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b717-134">-WhatIf</span></span>
<span data-ttu-id="5b717-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5b717-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b717-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5b717-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b717-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b717-137">CommonParameters</span></span>
<span data-ttu-id="5b717-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5b717-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b717-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5b717-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b717-140">輸入</span><span class="sxs-lookup"><span data-stu-id="5b717-140">INPUTS</span></span>

### <span data-ttu-id="5b717-141">System.object</span><span class="sxs-lookup"><span data-stu-id="5b717-141">System.String</span></span>
<span data-ttu-id="5b717-142">PSSnapshotUpdate PSSnapshot 中的 [計算] 的 [計算] 命令. []。</span><span class="sxs-lookup"><span data-stu-id="5b717-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="5b717-143">輸出</span><span class="sxs-lookup"><span data-stu-id="5b717-143">OUTPUTS</span></span>

### <span data-ttu-id="5b717-144">PSSnapshot 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="5b717-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="5b717-145">筆記</span><span class="sxs-lookup"><span data-stu-id="5b717-145">NOTES</span></span>

## <span data-ttu-id="5b717-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b717-146">RELATED LINKS</span></span>
