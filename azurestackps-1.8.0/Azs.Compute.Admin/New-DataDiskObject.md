---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b37d41ae2ec772cc755436bc01c3c4009c9c30f5
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793545"
---
# <span data-ttu-id="6cac5-101">New-DataDiskObject</span><span class="sxs-lookup"><span data-stu-id="6cac5-101">New-DataDiskObject</span></span>

## <span data-ttu-id="6cac5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6cac5-102">SYNOPSIS</span></span>
<span data-ttu-id="6cac5-103">建立用來建立新的虛擬機器平臺影像的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="6cac5-103">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

## <span data-ttu-id="6cac5-104">句法</span><span class="sxs-lookup"><span data-stu-id="6cac5-104">SYNTAX</span></span>

```
New-DataDiskObject [[-Lun] <Int32>] [[-Uri] <String>] [<CommonParameters>]
```

## <span data-ttu-id="6cac5-105">說明</span><span class="sxs-lookup"><span data-stu-id="6cac5-105">DESCRIPTION</span></span>
<span data-ttu-id="6cac5-106">建立擁有資料磁片相關資訊的物件。</span><span class="sxs-lookup"><span data-stu-id="6cac5-106">Creates an object holding information about a data disk.</span></span>

## <span data-ttu-id="6cac5-107">示例</span><span class="sxs-lookup"><span data-stu-id="6cac5-107">EXAMPLES</span></span>

### <span data-ttu-id="6cac5-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6cac5-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-DataDiskObject -Lun 5 -URI test.blob.windows.net/disks/datadisk5.vhd
```

<span data-ttu-id="6cac5-109">建立新的資料磁片盤物件。</span><span class="sxs-lookup"><span data-stu-id="6cac5-109">Create a new data disk object.</span></span>

## <span data-ttu-id="6cac5-110">參數</span><span class="sxs-lookup"><span data-stu-id="6cac5-110">PARAMETERS</span></span>

### <span data-ttu-id="6cac5-111">-Lun</span><span class="sxs-lookup"><span data-stu-id="6cac5-111">-Lun</span></span>
<span data-ttu-id="6cac5-112">邏輯單元號碼。</span><span class="sxs-lookup"><span data-stu-id="6cac5-112">Logical unit number.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cac5-113">-Uri</span><span class="sxs-lookup"><span data-stu-id="6cac5-113">-Uri</span></span>
<span data-ttu-id="6cac5-114">磁片模版的位置。</span><span class="sxs-lookup"><span data-stu-id="6cac5-114">Location of the disk template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cac5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cac5-115">CommonParameters</span></span>
<span data-ttu-id="6cac5-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6cac5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cac5-117">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6cac5-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cac5-118">輸入</span><span class="sxs-lookup"><span data-stu-id="6cac5-118">INPUTS</span></span>

## <span data-ttu-id="6cac5-119">輸出</span><span class="sxs-lookup"><span data-stu-id="6cac5-119">OUTPUTS</span></span>

## <span data-ttu-id="6cac5-120">筆記</span><span class="sxs-lookup"><span data-stu-id="6cac5-120">NOTES</span></span>

## <span data-ttu-id="6cac5-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="6cac5-121">RELATED LINKS</span></span>
