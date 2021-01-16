---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
ms.openlocfilehash: 677382133dffc7e64c86d02e984f35b8572a4598
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435268"
---
# <span data-ttu-id="f0d78-101">Get-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="f0d78-101">Get-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="f0d78-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f0d78-102">SYNOPSIS</span></span>
<span data-ttu-id="f0d78-103">取得 (ANF) 帳戶的 Azure NetApp 檔案的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f0d78-103">Gets details of an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="f0d78-104">句法</span><span class="sxs-lookup"><span data-stu-id="f0d78-104">SYNTAX</span></span>

### <span data-ttu-id="f0d78-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f0d78-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesAccount -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0d78-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0d78-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0d78-107">說明</span><span class="sxs-lookup"><span data-stu-id="f0d78-107">DESCRIPTION</span></span>
<span data-ttu-id="f0d78-108">**AzNetAppFilesAccount** Cmdlet 會取得 ANF 帳戶的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f0d78-108">The **Get-AzNetAppFilesAccount** cmdlet gets details of an ANF account.</span></span>

## <span data-ttu-id="f0d78-109">示例</span><span class="sxs-lookup"><span data-stu-id="f0d78-109">EXAMPLES</span></span>

### <span data-ttu-id="f0d78-110">範例1：取得 ANF 帳戶</span><span class="sxs-lookup"><span data-stu-id="f0d78-110">Example 1: Get an ANF account</span></span>
```
PS C:\>Get-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="f0d78-111">這個命令會取得名為 MyAnfAccount 的帳戶。</span><span class="sxs-lookup"><span data-stu-id="f0d78-111">This command gets the account named MyAnfAccount.</span></span>

## <span data-ttu-id="f0d78-112">參數</span><span class="sxs-lookup"><span data-stu-id="f0d78-112">PARAMETERS</span></span>

### <span data-ttu-id="f0d78-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0d78-113">-DefaultProfile</span></span>
<span data-ttu-id="f0d78-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0d78-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0d78-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f0d78-115">-Name</span></span>
<span data-ttu-id="f0d78-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="f0d78-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d78-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0d78-117">-ResourceGroupName</span></span>
<span data-ttu-id="f0d78-118">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="f0d78-118">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="f0d78-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0d78-119">-ResourceId</span></span>
<span data-ttu-id="f0d78-120">ANF 帳戶的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f0d78-120">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="f0d78-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0d78-121">CommonParameters</span></span>
<span data-ttu-id="f0d78-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f0d78-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0d78-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f0d78-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0d78-124">輸入</span><span class="sxs-lookup"><span data-stu-id="f0d78-124">INPUTS</span></span>

### <span data-ttu-id="f0d78-125">System.object</span><span class="sxs-lookup"><span data-stu-id="f0d78-125">System.String</span></span>

## <span data-ttu-id="f0d78-126">輸出</span><span class="sxs-lookup"><span data-stu-id="f0d78-126">OUTPUTS</span></span>

### <span data-ttu-id="f0d78-127">PSNetAppFilesAccount 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="f0d78-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="f0d78-128">筆記</span><span class="sxs-lookup"><span data-stu-id="f0d78-128">NOTES</span></span>

## <span data-ttu-id="f0d78-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0d78-129">RELATED LINKS</span></span>