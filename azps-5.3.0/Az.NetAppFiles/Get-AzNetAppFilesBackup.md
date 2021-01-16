---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
ms.openlocfilehash: 46f6f5d7f9d843a9dd6d30053e9205e52be989d4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435261"
---
# <span data-ttu-id="fe6a1-101">Get-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="fe6a1-101">Get-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="fe6a1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe6a1-102">SYNOPSIS</span></span>
<span data-ttu-id="fe6a1-103">取得 Azure NetApp 檔案 (ANF) 備份的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fe6a1-103">Gets details of an Azure NetApp Files (ANF) Backup.</span></span>

## <span data-ttu-id="fe6a1-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe6a1-104">SYNTAX</span></span>

### <span data-ttu-id="fe6a1-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fe6a1-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackup -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 [-VolumeName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe6a1-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe6a1-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe6a1-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe6a1-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe6a1-108">說明</span><span class="sxs-lookup"><span data-stu-id="fe6a1-108">DESCRIPTION</span></span>
<span data-ttu-id="fe6a1-109">**AzNetAppFilesBackup** Cmdlet 會取得 ANF 備份的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fe6a1-109">The **Get-AzNetAppFilesBackup** cmdlet gets details of an ANF backup.</span></span>

## <span data-ttu-id="fe6a1-110">示例</span><span class="sxs-lookup"><span data-stu-id="fe6a1-110">EXAMPLES</span></span>

### <span data-ttu-id="fe6a1-111">範例1</span><span class="sxs-lookup"><span data-stu-id="fe6a1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="fe6a1-112">這個命令會從名為「MyVolume」的卷中取得名為「MyAnfAccount」的 backcup。</span><span class="sxs-lookup"><span data-stu-id="fe6a1-112">This command gets the backcup named "MyAnfAccount" from the volume named "MyVolume".</span></span>

## <span data-ttu-id="fe6a1-113">參數</span><span class="sxs-lookup"><span data-stu-id="fe6a1-113">PARAMETERS</span></span>

### <span data-ttu-id="fe6a1-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fe6a1-114">-AccountName</span></span>
<span data-ttu-id="fe6a1-115">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="fe6a1-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="fe6a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe6a1-116">-DefaultProfile</span></span>
<span data-ttu-id="fe6a1-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe6a1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe6a1-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="fe6a1-118">-Name</span></span>
<span data-ttu-id="fe6a1-119">ANF 備份的名稱</span><span class="sxs-lookup"><span data-stu-id="fe6a1-119">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6a1-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="fe6a1-120">-PoolName</span></span>
<span data-ttu-id="fe6a1-121">ANF 池的名稱</span><span class="sxs-lookup"><span data-stu-id="fe6a1-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="fe6a1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe6a1-122">-ResourceGroupName</span></span>
<span data-ttu-id="fe6a1-123">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="fe6a1-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="fe6a1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe6a1-124">-ResourceId</span></span>
<span data-ttu-id="fe6a1-125">ANF 備份的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="fe6a1-125">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="fe6a1-126">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="fe6a1-126">-VolumeName</span></span>
<span data-ttu-id="fe6a1-127">ANF 體積的名稱</span><span class="sxs-lookup"><span data-stu-id="fe6a1-127">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6a1-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="fe6a1-128">-VolumeObject</span></span>
<span data-ttu-id="fe6a1-129">包含要返回之備份的卷物件</span><span class="sxs-lookup"><span data-stu-id="fe6a1-129">The volume object containing the backup to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe6a1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe6a1-130">CommonParameters</span></span>
<span data-ttu-id="fe6a1-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe6a1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe6a1-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fe6a1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe6a1-133">輸入</span><span class="sxs-lookup"><span data-stu-id="fe6a1-133">INPUTS</span></span>

### <span data-ttu-id="fe6a1-134">System.object</span><span class="sxs-lookup"><span data-stu-id="fe6a1-134">System.String</span></span>

### <span data-ttu-id="fe6a1-135">PSNetAppFilesVolume 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="fe6a1-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="fe6a1-136">輸出</span><span class="sxs-lookup"><span data-stu-id="fe6a1-136">OUTPUTS</span></span>

### <span data-ttu-id="fe6a1-137">PSNetAppFilesBackup 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="fe6a1-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="fe6a1-138">筆記</span><span class="sxs-lookup"><span data-stu-id="fe6a1-138">NOTES</span></span>

## <span data-ttu-id="fe6a1-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe6a1-139">RELATED LINKS</span></span>