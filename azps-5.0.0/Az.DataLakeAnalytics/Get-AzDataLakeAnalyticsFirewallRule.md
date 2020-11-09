---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 40c44ff157fca6a276cac8ece508e9d540b526ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285104"
---
# <span data-ttu-id="74977-101">Get-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="74977-101">Get-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="74977-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74977-102">SYNOPSIS</span></span>
<span data-ttu-id="74977-103">從資料 Lake Analytics 帳戶檢索防火牆規則或防火牆規則清單。</span><span class="sxs-lookup"><span data-stu-id="74977-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="74977-104">句法</span><span class="sxs-lookup"><span data-stu-id="74977-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74977-105">說明</span><span class="sxs-lookup"><span data-stu-id="74977-105">DESCRIPTION</span></span>
<span data-ttu-id="74977-106">**AzDataLakeAnalyticsFirewallRule** Cmdlet 會從 Azure Data Lake Analytics 帳戶檢索防火牆規則或防火牆規則清單。</span><span class="sxs-lookup"><span data-stu-id="74977-106">The **Get-AzDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="74977-107">示例</span><span class="sxs-lookup"><span data-stu-id="74977-107">EXAMPLES</span></span>

### <span data-ttu-id="74977-108">範例1：取得防火牆規則</span><span class="sxs-lookup"><span data-stu-id="74977-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="74977-109">這個命令會從帳戶 "ContosoAdlAcct" 中取得名為「我的防火牆規則」的防火牆規則</span><span class="sxs-lookup"><span data-stu-id="74977-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="74977-110">範例2：列出所有防火牆規則</span><span class="sxs-lookup"><span data-stu-id="74977-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="74977-111">這個命令會從 [ContosoAdlAcct] 帳戶取得所有防火牆規則</span><span class="sxs-lookup"><span data-stu-id="74977-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="74977-112">參數</span><span class="sxs-lookup"><span data-stu-id="74977-112">PARAMETERS</span></span>

### <span data-ttu-id="74977-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="74977-113">-Account</span></span>
<span data-ttu-id="74977-114">要取得防火牆規則的資料 Lake Analytics 帳戶</span><span class="sxs-lookup"><span data-stu-id="74977-114">The Data Lake Analytics account to get the firewall rule from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74977-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74977-115">-DefaultProfile</span></span>
<span data-ttu-id="74977-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="74977-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74977-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="74977-117">-Name</span></span>
<span data-ttu-id="74977-118">防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="74977-118">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74977-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74977-119">-ResourceGroupName</span></span>
<span data-ttu-id="74977-120">要在其下檢索帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="74977-120">Name of resource group under which want to retrieve the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74977-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74977-121">CommonParameters</span></span>
<span data-ttu-id="74977-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74977-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74977-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="74977-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74977-124">輸入</span><span class="sxs-lookup"><span data-stu-id="74977-124">INPUTS</span></span>

### <span data-ttu-id="74977-125">System.object</span><span class="sxs-lookup"><span data-stu-id="74977-125">System.String</span></span>

## <span data-ttu-id="74977-126">輸出</span><span class="sxs-lookup"><span data-stu-id="74977-126">OUTPUTS</span></span>

### <span data-ttu-id="74977-127">DataLakeAnalyticsFirewallRule 中的 DataLakeAnalytics。</span><span class="sxs-lookup"><span data-stu-id="74977-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="74977-128">筆記</span><span class="sxs-lookup"><span data-stu-id="74977-128">NOTES</span></span>

## <span data-ttu-id="74977-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="74977-129">RELATED LINKS</span></span>