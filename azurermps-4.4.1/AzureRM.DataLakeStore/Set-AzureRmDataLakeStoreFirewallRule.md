---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 30a1599468851da5f01e10dc94af6586d3ecaf8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624826"
---
# <span data-ttu-id="d022f-101">Set-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d022f-101">Set-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="d022f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d022f-102">SYNOPSIS</span></span>
<span data-ttu-id="d022f-103">修改指定資料 Lake Store 中的指定防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="d022f-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d022f-104">句法</span><span class="sxs-lookup"><span data-stu-id="d022f-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d022f-105">說明</span><span class="sxs-lookup"><span data-stu-id="d022f-105">DESCRIPTION</span></span>
<span data-ttu-id="d022f-106">**AzureRmDataLakeStoreFirewallRule** Cmdlet 會修改指定資料 Lake store 中的指定防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="d022f-106">The **Set-AzureRmDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="d022f-107">示例</span><span class="sxs-lookup"><span data-stu-id="d022f-107">EXAMPLES</span></span>

### <span data-ttu-id="d022f-108">範例1：更新防火牆規則的開始和結束 IP 範圍</span><span class="sxs-lookup"><span data-stu-id="d022f-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="d022f-109">更新帳戶 "ContosoADL" 中的防火牆規則 "MyFirewallRule" 以包含127.0.0.1 範圍（127.0.0.1）127.0.0。2</span><span class="sxs-lookup"><span data-stu-id="d022f-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="d022f-110">參數</span><span class="sxs-lookup"><span data-stu-id="d022f-110">PARAMETERS</span></span>

### <span data-ttu-id="d022f-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="d022f-111">-Account</span></span>
<span data-ttu-id="d022f-112">要在其中更新防火牆規則的 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="d022f-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="d022f-113">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="d022f-113">-EndIpAddress</span></span>
<span data-ttu-id="d022f-114">防火牆規則有效 ip 範圍的結尾</span><span class="sxs-lookup"><span data-stu-id="d022f-114">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d022f-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="d022f-115">-Name</span></span>
<span data-ttu-id="d022f-116">防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="d022f-116">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d022f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d022f-117">-ResourceGroupName</span></span>
<span data-ttu-id="d022f-118">指定包含要更新防火牆規則之帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d022f-118">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d022f-119">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="d022f-119">-StartIpAddress</span></span>
<span data-ttu-id="d022f-120">防火牆規則的有效 ip 範圍起點</span><span class="sxs-lookup"><span data-stu-id="d022f-120">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="d022f-121">-確認</span><span class="sxs-lookup"><span data-stu-id="d022f-121">-Confirm</span></span>
<span data-ttu-id="d022f-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d022f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d022f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d022f-123">-WhatIf</span></span>
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

### <span data-ttu-id="d022f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d022f-124">-DefaultProfile</span></span>
<span data-ttu-id="d022f-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d022f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d022f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d022f-126">CommonParameters</span></span>
<span data-ttu-id="d022f-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d022f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d022f-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d022f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d022f-129">輸入</span><span class="sxs-lookup"><span data-stu-id="d022f-129">INPUTS</span></span>

## <span data-ttu-id="d022f-130">輸出</span><span class="sxs-lookup"><span data-stu-id="d022f-130">OUTPUTS</span></span>

### <span data-ttu-id="d022f-131">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d022f-131">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="d022f-132">更新的防火牆規則的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d022f-132">The details of the updated firewall rule.</span></span>

## <span data-ttu-id="d022f-133">筆記</span><span class="sxs-lookup"><span data-stu-id="d022f-133">NOTES</span></span>

## <span data-ttu-id="d022f-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="d022f-134">RELATED LINKS</span></span>
