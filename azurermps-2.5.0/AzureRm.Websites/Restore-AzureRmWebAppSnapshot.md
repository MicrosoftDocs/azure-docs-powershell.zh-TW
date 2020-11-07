---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappsnapshot
schema: 2.0.0
ms.openlocfilehash: 0719210cae275dc7e250e7fd14e622c51014d7c2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801853"
---
# <span data-ttu-id="e54e6-101">Restore-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="e54e6-101">Restore-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="e54e6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e54e6-102">SYNOPSIS</span></span>
<span data-ttu-id="e54e6-103">還原 web 應用程式快照。</span><span class="sxs-lookup"><span data-stu-id="e54e6-103">Restores a web app snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e54e6-104">句法</span><span class="sxs-lookup"><span data-stu-id="e54e6-104">SYNTAX</span></span>

### <span data-ttu-id="e54e6-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="e54e6-105">FromResourceName</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e54e6-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="e54e6-106">FromWebApp</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e54e6-107">說明</span><span class="sxs-lookup"><span data-stu-id="e54e6-107">DESCRIPTION</span></span>
<span data-ttu-id="e54e6-108">將 web 應用程式快照還原至 web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="e54e6-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="e54e6-109">還原快照時，會使用快照中包含的檔案，覆寫 web app 中的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="e54e6-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="e54e6-110">若要同時還原設定，請使用 RecoverConfiguration 切換參數。</span><span class="sxs-lookup"><span data-stu-id="e54e6-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="e54e6-111">您可以將來自單一 web 應用程式的快照還原至相同訂閱中的任何其他 web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="e54e6-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="e54e6-112">示例</span><span class="sxs-lookup"><span data-stu-id="e54e6-112">EXAMPLES</span></span>

### <span data-ttu-id="e54e6-113">範例1</span><span class="sxs-lookup"><span data-stu-id="e54e6-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="e54e6-114">取得名為「ContosoApp」的 web 應用程式的最新快照，其中包含「Default-Web-WestUS」資源群組中名為「暫存」的槽。</span><span class="sxs-lookup"><span data-stu-id="e54e6-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="e54e6-115">將快照還原至 web 應用程式的「還原」槽。</span><span class="sxs-lookup"><span data-stu-id="e54e6-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="e54e6-116">參數</span><span class="sxs-lookup"><span data-stu-id="e54e6-116">PARAMETERS</span></span>

### <span data-ttu-id="e54e6-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e54e6-117">-AsJob</span></span>
<span data-ttu-id="e54e6-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e54e6-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e54e6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e54e6-119">-DefaultProfile</span></span>
<span data-ttu-id="e54e6-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e54e6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e54e6-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e54e6-121">-Force</span></span>
<span data-ttu-id="e54e6-122">允許覆蓋原始的 web 應用程式，而不顯示警告。</span><span class="sxs-lookup"><span data-stu-id="e54e6-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e54e6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e54e6-123">-InputObject</span></span>
<span data-ttu-id="e54e6-124">Azure Web App 快照。</span><span class="sxs-lookup"><span data-stu-id="e54e6-124">The Azure Web App snapshot.</span></span>
```yaml
Type: AzureWebAppSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e54e6-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="e54e6-125">-Name</span></span>
<span data-ttu-id="e54e6-126">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="e54e6-126">The name of the web app.</span></span>
```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e54e6-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="e54e6-127">-RecoverConfiguration</span></span>
<span data-ttu-id="e54e6-128">除了檔案之外，還能復原 web 應用程式的配置。</span><span class="sxs-lookup"><span data-stu-id="e54e6-128">Recover the web app's configuration in addition to files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e54e6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e54e6-129">-ResourceGroupName</span></span>
<span data-ttu-id="e54e6-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e54e6-130">The name of the resource group.</span></span>
```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e54e6-131">-槽</span><span class="sxs-lookup"><span data-stu-id="e54e6-131">-Slot</span></span>
<span data-ttu-id="e54e6-132">Web 應用程式槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="e54e6-132">The name of the web app slot.</span></span>
```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e54e6-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e54e6-133">-WebApp</span></span>
<span data-ttu-id="e54e6-134">Web app 物件</span><span class="sxs-lookup"><span data-stu-id="e54e6-134">The web app object</span></span>
```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e54e6-135">-確認</span><span class="sxs-lookup"><span data-stu-id="e54e6-135">-Confirm</span></span>
<span data-ttu-id="e54e6-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e54e6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e54e6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e54e6-137">-WhatIf</span></span>
<span data-ttu-id="e54e6-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e54e6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e54e6-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e54e6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e54e6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e54e6-140">CommonParameters</span></span>
<span data-ttu-id="e54e6-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e54e6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e54e6-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e54e6-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e54e6-143">輸入</span><span class="sxs-lookup"><span data-stu-id="e54e6-143">INPUTS</span></span>

### <span data-ttu-id="e54e6-144">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="e54e6-144">System.Management.Automation.SwitchParameter</span></span>
<span data-ttu-id="e54e6-145">BackupRestore AzureWebAppSnapshot System. WebApps..............。</span><span class="sxs-lookup"><span data-stu-id="e54e6-145">Microsoft.Azure.Management.WebSites.Models.Site System.String Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot System.DateTime</span></span>

## <span data-ttu-id="e54e6-146">輸出</span><span class="sxs-lookup"><span data-stu-id="e54e6-146">OUTPUTS</span></span>

### <span data-ttu-id="e54e6-147">System.object</span><span class="sxs-lookup"><span data-stu-id="e54e6-147">System.Object</span></span>

## <span data-ttu-id="e54e6-148">筆記</span><span class="sxs-lookup"><span data-stu-id="e54e6-148">NOTES</span></span>

## <span data-ttu-id="e54e6-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="e54e6-149">RELATED LINKS</span></span>
