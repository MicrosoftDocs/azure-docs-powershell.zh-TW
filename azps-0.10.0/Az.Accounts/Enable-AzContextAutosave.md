---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6c0e557078bde5cbec7b1f7dd96f1fa2c71408a7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794146"
---
# <span data-ttu-id="8119f-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="8119f-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="8119f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8119f-102">SYNOPSIS</span></span>
<span data-ttu-id="8119f-103">允許在您開啟 PowerShell 視窗時，儲存 azure 認證、帳戶和訂閱資訊，並自動載入。</span><span class="sxs-lookup"><span data-stu-id="8119f-103">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="8119f-104">句法</span><span class="sxs-lookup"><span data-stu-id="8119f-104">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8119f-105">說明</span><span class="sxs-lookup"><span data-stu-id="8119f-105">DESCRIPTION</span></span>
<span data-ttu-id="8119f-106">允許在您開啟 PowerShell 視窗時，儲存 azure 認證、帳戶和訂閱資訊，並自動載入。</span><span class="sxs-lookup"><span data-stu-id="8119f-106">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="8119f-107">示例</span><span class="sxs-lookup"><span data-stu-id="8119f-107">EXAMPLES</span></span>

### <span data-ttu-id="8119f-108">為目前的使用者啟用 autosaving 認證</span><span class="sxs-lookup"><span data-stu-id="8119f-108">Enable autosaving credentials for the current user</span></span>
```
PS C:\> Enable-AzContextAutosave
```

<span data-ttu-id="8119f-109">針對目前的使用者開啟認證自動儲存。</span><span class="sxs-lookup"><span data-stu-id="8119f-109">Turn on credential autosave for the current user.</span></span>  <span data-ttu-id="8119f-110">每當開啟 powershell 視窗時，就會記住您目前的內容，而不需要登入。</span><span class="sxs-lookup"><span data-stu-id="8119f-110">Whenever a powershell window is opened, your current context will be remembered without logging in.</span></span>

## <span data-ttu-id="8119f-111">參數</span><span class="sxs-lookup"><span data-stu-id="8119f-111">PARAMETERS</span></span>

### <span data-ttu-id="8119f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8119f-112">-DefaultProfile</span></span>
<span data-ttu-id="8119f-113">用於與 azure 進行通訊的認證、租使用者與訂閱</span><span class="sxs-lookup"><span data-stu-id="8119f-113">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8119f-114">-範圍</span><span class="sxs-lookup"><span data-stu-id="8119f-114">-Scope</span></span>
<span data-ttu-id="8119f-115">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話</span><span class="sxs-lookup"><span data-stu-id="8119f-115">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8119f-116">-確認</span><span class="sxs-lookup"><span data-stu-id="8119f-116">-Confirm</span></span>
<span data-ttu-id="8119f-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8119f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8119f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8119f-118">-WhatIf</span></span>
<span data-ttu-id="8119f-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8119f-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8119f-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8119f-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8119f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8119f-121">CommonParameters</span></span>
<span data-ttu-id="8119f-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8119f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8119f-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8119f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8119f-124">輸入</span><span class="sxs-lookup"><span data-stu-id="8119f-124">INPUTS</span></span>

### <span data-ttu-id="8119f-125">所有</span><span class="sxs-lookup"><span data-stu-id="8119f-125">None</span></span>

## <span data-ttu-id="8119f-126">輸出</span><span class="sxs-lookup"><span data-stu-id="8119f-126">OUTPUTS</span></span>

### <span data-ttu-id="8119f-127">CoNtextAutosaveSettings 的常見驗證。</span><span class="sxs-lookup"><span data-stu-id="8119f-127">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="8119f-128">筆記</span><span class="sxs-lookup"><span data-stu-id="8119f-128">NOTES</span></span>

## <span data-ttu-id="8119f-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="8119f-129">RELATED LINKS</span></span>