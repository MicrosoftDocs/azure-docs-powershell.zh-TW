---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
ms.openlocfilehash: 010698183dec206002c0966fb8f37d629d24794a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284675"
---
# <span data-ttu-id="f8d34-101">New-AzAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="f8d34-101">New-AzAutoscaleNotification</span></span>

## <span data-ttu-id="f8d34-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f8d34-102">SYNOPSIS</span></span>
<span data-ttu-id="f8d34-103">建立自動縮放電子郵件通知。</span><span class="sxs-lookup"><span data-stu-id="f8d34-103">Creates an Autoscale email notification.</span></span>

## <span data-ttu-id="f8d34-104">句法</span><span class="sxs-lookup"><span data-stu-id="f8d34-104">SYNTAX</span></span>

```
New-AzAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8d34-105">說明</span><span class="sxs-lookup"><span data-stu-id="f8d34-105">DESCRIPTION</span></span>
<span data-ttu-id="f8d34-106">**新的-AzAutoscaleNotification** Cmdlet 會建立自動縮放的電子郵件通知。</span><span class="sxs-lookup"><span data-stu-id="f8d34-106">The **New-AzAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="f8d34-107">示例</span><span class="sxs-lookup"><span data-stu-id="f8d34-107">EXAMPLES</span></span>

### <span data-ttu-id="f8d34-108">範例1：建立自動縮放電子郵件通知</span><span class="sxs-lookup"><span data-stu-id="f8d34-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzAutoscaleNotification -CustomEmail "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="f8d34-109">這個命令會建立兩個指定位址的 Autosacale 電子郵件通知。</span><span class="sxs-lookup"><span data-stu-id="f8d34-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="f8d34-110">範例2：為訂閱管理員建立自動縮放電子郵件通知</span><span class="sxs-lookup"><span data-stu-id="f8d34-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="f8d34-111">這個命令會建立訂閱系統管理員的 Autosacale 電子郵件通知。</span><span class="sxs-lookup"><span data-stu-id="f8d34-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="f8d34-112">參數</span><span class="sxs-lookup"><span data-stu-id="f8d34-112">PARAMETERS</span></span>

### <span data-ttu-id="f8d34-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="f8d34-113">-CustomEmail</span></span>
<span data-ttu-id="f8d34-114">指定以逗號分隔的電子郵件地址清單。</span><span class="sxs-lookup"><span data-stu-id="f8d34-114">Specifies a comma-separated list of email addresses.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8d34-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8d34-115">-DefaultProfile</span></span>
<span data-ttu-id="f8d34-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f8d34-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8d34-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="f8d34-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="f8d34-118">表示此操作會傳送電子郵件通知給訂閱管理員。</span><span class="sxs-lookup"><span data-stu-id="f8d34-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8d34-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="f8d34-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="f8d34-120">表示此操作會傳送電子郵件通知給訂閱共同管理員。</span><span class="sxs-lookup"><span data-stu-id="f8d34-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8d34-121">-Webhook</span><span class="sxs-lookup"><span data-stu-id="f8d34-121">-Webhook</span></span>
<span data-ttu-id="f8d34-122">指定以逗號分隔的自動縮放 webhooks 清單。</span><span class="sxs-lookup"><span data-stu-id="f8d34-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8d34-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8d34-123">CommonParameters</span></span>
<span data-ttu-id="f8d34-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f8d34-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8d34-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f8d34-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8d34-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f8d34-126">INPUTS</span></span>

### <span data-ttu-id="f8d34-127">WebhookNotification [] 中的 [管理模型]</span><span class="sxs-lookup"><span data-stu-id="f8d34-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="f8d34-128">System.object []</span><span class="sxs-lookup"><span data-stu-id="f8d34-128">System.String[]</span></span>

### <span data-ttu-id="f8d34-129">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="f8d34-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f8d34-130">輸出</span><span class="sxs-lookup"><span data-stu-id="f8d34-130">OUTPUTS</span></span>

### <span data-ttu-id="f8d34-131">AutoscaleNotification 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="f8d34-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="f8d34-132">筆記</span><span class="sxs-lookup"><span data-stu-id="f8d34-132">NOTES</span></span>

## <span data-ttu-id="f8d34-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8d34-133">RELATED LINKS</span></span>

[<span data-ttu-id="f8d34-134">新-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="f8d34-134">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)

