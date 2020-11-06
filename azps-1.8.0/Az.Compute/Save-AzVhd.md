---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVhd.md
ms.openlocfilehash: 7fccc80dcd882253a656e403109d43da07ab111d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622705"
---
# <span data-ttu-id="c3893-101">Save-AzVhd</span><span class="sxs-lookup"><span data-stu-id="c3893-101">Save-AzVhd</span></span>

## <span data-ttu-id="c3893-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c3893-102">SYNOPSIS</span></span>
<span data-ttu-id="c3893-103">在本機儲存已下載的 .vhd 影像。</span><span class="sxs-lookup"><span data-stu-id="c3893-103">Saves downloaded .vhd images locally.</span></span>

## <span data-ttu-id="c3893-104">句法</span><span class="sxs-lookup"><span data-stu-id="c3893-104">SYNTAX</span></span>

### <span data-ttu-id="c3893-105">ResourceGroupParameterSetName</span><span class="sxs-lookup"><span data-stu-id="c3893-105">ResourceGroupParameterSetName</span></span>
```
Save-AzVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c3893-106">StorageKeyParameterSetName</span><span class="sxs-lookup"><span data-stu-id="c3893-106">StorageKeyParameterSetName</span></span>
```
Save-AzVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfThreads] <Int32>]
 [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3893-107">說明</span><span class="sxs-lookup"><span data-stu-id="c3893-107">DESCRIPTION</span></span>
<span data-ttu-id="c3893-108">**AzVhd** Cmdlet 會從 blob 儲存 .vhd 影像，在其中儲存在檔案中。</span><span class="sxs-lookup"><span data-stu-id="c3893-108">The **Save-AzVhd** cmdlet saves .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="c3893-109">您可以指定進程所使用的下載程式執行緒數，以及是否要取代現有的檔案。</span><span class="sxs-lookup"><span data-stu-id="c3893-109">You can specify the number of downloader threads that the process uses and whether to replace a file that already exists.</span></span>
<span data-ttu-id="c3893-110">這個 Cmdlet 會下載內容。</span><span class="sxs-lookup"><span data-stu-id="c3893-110">This cmdlet downloads content as it is.</span></span>
<span data-ttu-id="c3893-111">它不會將任何虛擬硬碟 (VHD) 格式轉換。</span><span class="sxs-lookup"><span data-stu-id="c3893-111">It does not apply any Virtual Hard Disk (VHD) format conversion.</span></span>

## <span data-ttu-id="c3893-112">示例</span><span class="sxs-lookup"><span data-stu-id="c3893-112">EXAMPLES</span></span>

### <span data-ttu-id="c3893-113">範例1：下載影像</span><span class="sxs-lookup"><span data-stu-id="c3893-113">Example 1: Download an image</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -ResourceGroupName "rgname"
```

<span data-ttu-id="c3893-114">這個命令會下載 .vhd 檔案，並將它儲存在本機路徑 C:\vhd\Win7Image.vhd。</span><span class="sxs-lookup"><span data-stu-id="c3893-114">This command downloads a .vhd file, and stores it in the local path C:\vhd\Win7Image.vhd.</span></span>

### <span data-ttu-id="c3893-115">範例2：下載影像並覆寫本機檔案</span><span class="sxs-lookup"><span data-stu-id="c3893-115">Example 2: Download an image and overwrite the local file</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite -ResourceGroupName "rgname"
```

<span data-ttu-id="c3893-116">這個命令會下載 .vhd 檔案，並儲存在本機路徑中。</span><span class="sxs-lookup"><span data-stu-id="c3893-116">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="c3893-117">此命令包含 *Overwrite* 參數。</span><span class="sxs-lookup"><span data-stu-id="c3893-117">The command includes the *Overwrite* parameter.</span></span>
<span data-ttu-id="c3893-118">因此，如果 C:\vhd\Win7Image.vhd 已存在，此命令就會將它取代。</span><span class="sxs-lookup"><span data-stu-id="c3893-118">Therefore, if C:\vhd\Win7Image.vhd already exists, this command replaces it.</span></span>

### <span data-ttu-id="c3893-119">範例3：使用指定的執行緒數下載影像</span><span class="sxs-lookup"><span data-stu-id="c3893-119">Example 3: Download an image by using a specified number of threads</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32 -ResourceGroupName "rgname"
```

<span data-ttu-id="c3893-120">這個命令會下載 .vhd 檔案，並儲存在本機路徑中。</span><span class="sxs-lookup"><span data-stu-id="c3893-120">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="c3893-121">該命令會將 *NumberOfThreads* 參數的值指定為32。</span><span class="sxs-lookup"><span data-stu-id="c3893-121">The command specifies a value of 32 for the *NumberOfThreads* parameter.</span></span>
<span data-ttu-id="c3893-122">因此，該 Cmdlet 會針對此動作使用32執行緒。</span><span class="sxs-lookup"><span data-stu-id="c3893-122">Therefore, the cmdlet uses 32 threads for this action.</span></span>

### <span data-ttu-id="c3893-123">範例4：下載影像並指定存儲金鑰</span><span class="sxs-lookup"><span data-stu-id="c3893-123">Example 4: Download an image and specify the storage key</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw==" -ResourceGroupName "rgname"
```

<span data-ttu-id="c3893-124">這個命令會下載 .vhd 檔案，並指定存儲金鑰。</span><span class="sxs-lookup"><span data-stu-id="c3893-124">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="c3893-125">參數</span><span class="sxs-lookup"><span data-stu-id="c3893-125">PARAMETERS</span></span>

### <span data-ttu-id="c3893-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3893-126">-AsJob</span></span>
<span data-ttu-id="c3893-127">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="c3893-127">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c3893-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3893-128">-DefaultProfile</span></span>
<span data-ttu-id="c3893-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c3893-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3893-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="c3893-130">-LocalFilePath</span></span>
<span data-ttu-id="c3893-131">指定已儲存影像的本機檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="c3893-131">Specifies the local file path of the saved image.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3893-132">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="c3893-132">-NumberOfThreads</span></span>
<span data-ttu-id="c3893-133">指定此 Cmdlet 在下載期間使用的下載執行緒數。</span><span class="sxs-lookup"><span data-stu-id="c3893-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3893-134">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="c3893-134">-OverWrite</span></span>
<span data-ttu-id="c3893-135">表示此 Cmdlet 會取代 *LocalFilePath* 檔案所指定的檔案（如果存在的話）。</span><span class="sxs-lookup"><span data-stu-id="c3893-135">Indicates that this cmdlet replaces the file specified by *LocalFilePath* file if it exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3893-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3893-136">-ResourceGroupName</span></span>
<span data-ttu-id="c3893-137">指定儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3893-137">Specifies the name of the resource group of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3893-138">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="c3893-138">-SourceUri</span></span>
<span data-ttu-id="c3893-139">指定中 blob 的統一資源識別項 (URI) `Azure` 。</span><span class="sxs-lookup"><span data-stu-id="c3893-139">Specifies the Uniform Resource Identifier (URI) of the blob in `Azure`.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: src, Source

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3893-140">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="c3893-140">-StorageKey</span></span>
<span data-ttu-id="c3893-141">指定 [blob 儲存空間] 帳戶的儲存空間。</span><span class="sxs-lookup"><span data-stu-id="c3893-141">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="c3893-142">如果您沒有指定金鑰，這個 Cmdlet 會嘗試從 Azure 判斷 *SourceUri* 中帳戶的儲存金鑰。</span><span class="sxs-lookup"><span data-stu-id="c3893-142">If you do not specify a key, this cmdlet attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageKeyParameterSetName
Aliases: sk

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3893-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3893-143">CommonParameters</span></span>
<span data-ttu-id="c3893-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c3893-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3893-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c3893-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3893-146">輸入</span><span class="sxs-lookup"><span data-stu-id="c3893-146">INPUTS</span></span>

### <span data-ttu-id="c3893-147">System.object</span><span class="sxs-lookup"><span data-stu-id="c3893-147">System.String</span></span>

### <span data-ttu-id="c3893-148">系統 Uri</span><span class="sxs-lookup"><span data-stu-id="c3893-148">System.Uri</span></span>

## <span data-ttu-id="c3893-149">輸出</span><span class="sxs-lookup"><span data-stu-id="c3893-149">OUTPUTS</span></span>

### <span data-ttu-id="c3893-150">VhdDownloadCoNtext 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="c3893-150">Microsoft.Azure.Commands.Compute.Models.VhdDownloadContext</span></span>

## <span data-ttu-id="c3893-151">筆記</span><span class="sxs-lookup"><span data-stu-id="c3893-151">NOTES</span></span>

## <span data-ttu-id="c3893-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3893-152">RELATED LINKS</span></span>

[<span data-ttu-id="c3893-153">附加 AzVhd</span><span class="sxs-lookup"><span data-stu-id="c3893-153">Add-AzVhd</span></span>](./Add-AzVhd.md)

