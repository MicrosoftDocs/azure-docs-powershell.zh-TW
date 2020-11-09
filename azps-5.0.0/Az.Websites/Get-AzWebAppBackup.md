---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: e8c3f7543062613527e7f52be2cd6493f53c5f60
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286196"
---
# <span data-ttu-id="d87f9-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="d87f9-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="d87f9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d87f9-102">SYNOPSIS</span></span>

## <span data-ttu-id="d87f9-103">句法</span><span class="sxs-lookup"><span data-stu-id="d87f9-103">SYNTAX</span></span>

### <span data-ttu-id="d87f9-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="d87f9-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d87f9-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="d87f9-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d87f9-106">說明</span><span class="sxs-lookup"><span data-stu-id="d87f9-106">DESCRIPTION</span></span>
<span data-ttu-id="d87f9-107">**AzWebAppBackup** Cmdlet 會取得 Azure Web App 的指定備份。</span><span class="sxs-lookup"><span data-stu-id="d87f9-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="d87f9-108">示例</span><span class="sxs-lookup"><span data-stu-id="d87f9-108">EXAMPLES</span></span>

### <span data-ttu-id="d87f9-109">範例1</span><span class="sxs-lookup"><span data-stu-id="d87f9-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="d87f9-110">這個命令會從屬於資源群組 Default-Web WestUS 的名為「WebAppStandard」的 Web App 中，取得 ID 為「12345」的備份。</span><span class="sxs-lookup"><span data-stu-id="d87f9-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="d87f9-111">參數</span><span class="sxs-lookup"><span data-stu-id="d87f9-111">PARAMETERS</span></span>

### <span data-ttu-id="d87f9-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="d87f9-112">-BackupId</span></span>
<span data-ttu-id="d87f9-113">備份識別碼</span><span class="sxs-lookup"><span data-stu-id="d87f9-113">Backup Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d87f9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d87f9-114">-DefaultProfile</span></span>
<span data-ttu-id="d87f9-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d87f9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d87f9-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="d87f9-116">-Name</span></span>
<span data-ttu-id="d87f9-117">Webapp 名稱</span><span class="sxs-lookup"><span data-stu-id="d87f9-117">Webapp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d87f9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d87f9-118">-ResourceGroupName</span></span>
<span data-ttu-id="d87f9-119">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="d87f9-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d87f9-120">-槽</span><span class="sxs-lookup"><span data-stu-id="d87f9-120">-Slot</span></span>
<span data-ttu-id="d87f9-121">槽名稱</span><span class="sxs-lookup"><span data-stu-id="d87f9-121">Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d87f9-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d87f9-122">-WebApp</span></span>
<span data-ttu-id="d87f9-123">管道 WebApp</span><span class="sxs-lookup"><span data-stu-id="d87f9-123">Piped WebApp</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d87f9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d87f9-124">CommonParameters</span></span>
<span data-ttu-id="d87f9-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d87f9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d87f9-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d87f9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d87f9-127">輸入</span><span class="sxs-lookup"><span data-stu-id="d87f9-127">INPUTS</span></span>

### <span data-ttu-id="d87f9-128">System.object</span><span class="sxs-lookup"><span data-stu-id="d87f9-128">System.String</span></span>

### <span data-ttu-id="d87f9-129">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="d87f9-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d87f9-130">輸出</span><span class="sxs-lookup"><span data-stu-id="d87f9-130">OUTPUTS</span></span>

### <span data-ttu-id="d87f9-131">WebApps WebApps. AzureWebAppBackup （）</span><span class="sxs-lookup"><span data-stu-id="d87f9-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="d87f9-132">筆記</span><span class="sxs-lookup"><span data-stu-id="d87f9-132">NOTES</span></span>

## <span data-ttu-id="d87f9-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="d87f9-133">RELATED LINKS</span></span>